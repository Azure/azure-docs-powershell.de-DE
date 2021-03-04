---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServer.md
ms.openlocfilehash: 4d4581d78b2e1f90ce334fda77107058f2294f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941136"
---
# <span data-ttu-id="5fecc-101">New-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="5fecc-101">New-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="5fecc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fecc-102">SYNOPSIS</span></span>
<span data-ttu-id="5fecc-103">Erstellt einen neuen flexiblen MySQL-Server.</span><span class="sxs-lookup"><span data-stu-id="5fecc-103">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="5fecc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fecc-104">SYNTAX</span></span>

```
New-AzMySqlFlexibleServer [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AdministratorLoginPassword <SecureString>] [-AdministratorUserName <String>] [-BackupRetentionDay <Int32>]
 [-HighAvailability <Object>] [-Location <String>] [-PublicAccess <String>] [-Sku <String>]
 [-SkuTier <String>] [-StorageInMb <Int32>] [-Subnet <String>] [-SubnetPrefix <String>] [-Tag <Hashtable>]
 [-Version <ServerVersion>] [-Vnet <String>] [-VnetPrefix <String>] [-Zone <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5fecc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fecc-105">DESCRIPTION</span></span>
<span data-ttu-id="5fecc-106">Erstellt einen neuen flexiblen MySQL-Server.</span><span class="sxs-lookup"><span data-stu-id="5fecc-106">Creates a new MySQL flexible server.</span></span>

## <span data-ttu-id="5fecc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5fecc-107">EXAMPLES</span></span>

### <span data-ttu-id="5fecc-108">Beispiel 1: Erstellen eines neuen flexiblen MySql-Servers mit Argumenten</span><span class="sxs-lookup"><span data-stu-id="5fecc-108">Example 1: Create a new MySql flexible server with arguments</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest \
-Location eastus -AdministratorUserName mysqltest -AdministratorLoginPassword $password -Sku Standard_B1ms -SkuTier Burstable -Version 12 -StorageInMb 10240 -PublicAccess none

Checking the existence of the resource group PowershellMySqlTest ...
Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group MySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```



### <span data-ttu-id="5fecc-109">Beispiel 2: Erstellen eines neuen flexiblen MySql-Servers mit Standardeinstellung</span><span class="sxs-lookup"><span data-stu-id="5fecc-109">Example 2: Create a new MySql flexible server with default setting</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer

Creating resource group group00000000...
Creating new vnet VNETserver00000000 in resource group group00000000
Creating new subnet Subnetserver00000000 in resource group group00000000 and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group group00000000...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="5fecc-110">Dieses Cmdlet erstellt einen flexiblen MySql-Server mit Standardwerten, stellt den Server in einem neuen virtuellen Netzwerk zur Verfügung und hat ein Subnetz, das an den Server delegiert ist.</span><span class="sxs-lookup"><span data-stu-id="5fecc-110">This cmdlet creates MySql flexible server with default parameter values and provision the server inside a new virtual network and have a subnet delegated to the server.</span></span>
<span data-ttu-id="5fecc-111">Die Standardwerte des Speicherorts sind West US 2, Sku ist Standard_B1ms, Sku-Ebene ist Burstable und Speichergröße 10GiB.</span><span class="sxs-lookup"><span data-stu-id="5fecc-111">The default values of location is West US 2, Sku is Standard_B1ms, Sku tier is Burstable, and storage size is 10GiB.</span></span>


<span data-ttu-id="5fecc-112">Wenn Sie das automatisch generierte Kennwort für Ihren Server suchen möchten, verwenden Sie ConvertFrom-SecureString, um die Eigenschaft "SecuredPassword" in Nur-Text zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="5fecc-112">If you want to find the auto-generated password for your server, use ConvertFrom-SecureString to convert 'SecuredPassword' property to plain text.</span></span>

<span data-ttu-id="5fecc-113">(z. B. $server. SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span><span class="sxs-lookup"><span data-stu-id="5fecc-113">(E.g., $server.SecuredPassword | ConvertFrom-SecureString -AsPlainText)</span></span>

### <span data-ttu-id="5fecc-114">Beispiel 3: Erstellen eines neuen flexiblen MySql-Servers mit virtuellem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="5fecc-114">Example 3: Create a new MySql flexible server with virtual network</span></span>
```powershell
PS C:\> $Vnet = 'vnetname'
PS C:\> New-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

or

PS C:\> $Vnet = '/subscriptions/00000000-0000-0000-0000-0000000000/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/vnetname'
PS C:\> New-AzMySqlFlexibleServer  -ResourceGroupName PowershellMySqlTest -Vnet $Vnet

Resource group PowershellMySqlTest exists ? : True
You have supplied a vnet Id/name. Verifying its existence...
Creating new vnet vnetname in resource group PowershellMySqlTest
Creating new subnet Subnetserver00000000 in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server server00000000 in group PowershellMySqlTest...
Your server server00000000 is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="5fecc-115">Dieses Cmdlet erstellt einen flexiblen MySql-Server mit vnet-ID oder vnet-Namen, die von einem Benutzer bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5fecc-115">This cmdlet creates MySql flexible server with vnet id or vnet name provided by a user.</span></span>
<span data-ttu-id="5fecc-116">Wenn das virtuelle Netzwerk nicht vorhanden ist, erstellt das Cmdlet eins.</span><span class="sxs-lookup"><span data-stu-id="5fecc-116">If the virtual network doesn't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="5fecc-117">Beispiel 4: Erstellen eines neuen flexiblen MySql-Servers mit virtuellem Netzwerk- und Subnetznamen</span><span class="sxs-lookup"><span data-stu-id="5fecc-117">Example 4: Create a new MySql flexible server with virtual network and subnet name</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -Vnet mysql-vnet -Subnet mysql-subnet -VnetPrefix 10.0.0.0/16 -SubnetPrefix 10.0.0.0/24

Resource group PowershellMySqlTest exists ? : True
Creating new vnet mysql-vnet in resource group PowershellMySqlTest
Creating new subnet mysql-subnet in resource group PowershellMySqlTest and delegating it to Microsoft.DBforMySQL/flexibleServers
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="5fecc-118">Dieses Cmdlet erstellt einen flexiblen MySql-Server mit vnet-Namen, Subnetznamen, Vnetpräfix und Subnetzpräfix.</span><span class="sxs-lookup"><span data-stu-id="5fecc-118">This cmdlet creates MySql flexible server with vnet name, subnet name, vnet prefix, and subnet prefix.</span></span>
<span data-ttu-id="5fecc-119">Wenn das virtuelle Netzwerk und das Subnetz nicht vorhanden sind, erstellt das Cmdlet eins.</span><span class="sxs-lookup"><span data-stu-id="5fecc-119">If the virtual network and subnet don't exist, the cmdlet creates one.</span></span>

### <span data-ttu-id="5fecc-120">Beispiel 7: Erstellen eines neuen flexiblen MySql-Servers mit öffentlichem Zugriff auf alle IPs</span><span class="sxs-lookup"><span data-stu-id="5fecc-120">Example 7: Create a new MySql flexible server with public access to all IPs</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess All

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 0.0.0.0 to 255.255.255.255

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240
```

<span data-ttu-id="5fecc-121">Dieses Cmdlet erstellt einen flexiblen MySql-Server, der für alle IP-Adressen geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="5fecc-121">This cmdlet creates MySql flexible server open to all IP addresses.</span></span>

### <span data-ttu-id="5fecc-122">Beispiel 8: Erstellen eines neuen flexiblen MySql-Servers mit Firewall</span><span class="sxs-lookup"><span data-stu-id="5fecc-122">Example 8: Create a new MySql flexible server with firewall</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServer -Name mysql-test -ResourceGroupName PowershellMySqlTest -PublicAccess 10.10.10.10-10.10.10.12

Resource group PowershellMySqlTest exists ? : True
Creating MySQL server mysql-test in group PowershellMySqlTest...
Your server mysql-test is using sku Standard_B1ms (Paid Tier). Please refer to https://aka.ms/mysql-pricing for pricing details
Creating database flexibleserverdb...
Configuring server firewall rule to accept connections from 10.10.10.10 to 10.10.10.12

Name             Location  SkuName       SkuTier   AdministratorLogin Version StorageProfileStorageMb
----             --------  -------       -------   ------------------ ------- -----------------------
mysql-test       West US 2 Standard_B1ms Burstable mysqltest          5.7     10240

```

<span data-ttu-id="5fecc-123">Dieses Cmdlet erstellt einen flexiblen MySql-Server, der für angegebene IP-Adressen geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="5fecc-123">This cmdlet creates MySql flexible server open to specified IP addresses.</span></span>

## <span data-ttu-id="5fecc-124">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5fecc-124">PARAMETERS</span></span>

### <span data-ttu-id="5fecc-125">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="5fecc-125">-AdministratorLoginPassword</span></span>
<span data-ttu-id="5fecc-126">Das Kennwort des Administrators.</span><span class="sxs-lookup"><span data-stu-id="5fecc-126">The password of the administrator.</span></span>
<span data-ttu-id="5fecc-127">Mindestens 8 Zeichen und maximal 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5fecc-127">Minimum 8 characters and maximum 128 characters.</span></span>
<span data-ttu-id="5fecc-128">Das Kennwort muss Zeichen aus drei der folgenden Kategorien enthalten: englische Großbuchstaben, englische Kleinbuchstaben, Zahlen und nicht alphanumerische Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5fecc-128">Password must contain characters from three of the following categories: English uppercase letters, English lowercase letters, numbers, and non-alphanumeric characters.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-129">-AdministratorUserName</span><span class="sxs-lookup"><span data-stu-id="5fecc-129">-AdministratorUserName</span></span>
<span data-ttu-id="5fecc-130">Administratorname für den Server.</span><span class="sxs-lookup"><span data-stu-id="5fecc-130">Administrator username for the server.</span></span>
<span data-ttu-id="5fecc-131">Nachdem sie festgelegt wurde, kann sie nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5fecc-131">Once set, it cannot be changed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-132">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fecc-132">-AsJob</span></span>
<span data-ttu-id="5fecc-133">Führen Sie den Befehl als Auftrag aus.</span><span class="sxs-lookup"><span data-stu-id="5fecc-133">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-134">-BackupRetentionDay</span><span class="sxs-lookup"><span data-stu-id="5fecc-134">-BackupRetentionDay</span></span>
<span data-ttu-id="5fecc-135">Sicherungsaufbewahrungstage für den Server.</span><span class="sxs-lookup"><span data-stu-id="5fecc-135">Backup retention days for the server.</span></span>
<span data-ttu-id="5fecc-136">Die Tagesanzahl liegt zwischen 7 und 35.</span><span class="sxs-lookup"><span data-stu-id="5fecc-136">Day count is between 7 and 35.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fecc-137">-DefaultProfile</span></span>
<span data-ttu-id="5fecc-138">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fecc-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-139">-HighAvailability</span><span class="sxs-lookup"><span data-stu-id="5fecc-139">-HighAvailability</span></span>
<span data-ttu-id="5fecc-140">Aktivieren oder Deaktivieren des Features für hohe Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="5fecc-140">Enable or disable high availability feature.</span></span>
<span data-ttu-id="5fecc-141">Der Standardwert ist Deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5fecc-141">Default value is Disabled.</span></span>
<span data-ttu-id="5fecc-142">Standard: Deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5fecc-142">Default: Disabled.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-143">-Location</span><span class="sxs-lookup"><span data-stu-id="5fecc-143">-Location</span></span>
<span data-ttu-id="5fecc-144">Der Speicherort, an dem sich die Ressource befindet.</span><span class="sxs-lookup"><span data-stu-id="5fecc-144">The location the resource resides in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-145">-Name</span><span class="sxs-lookup"><span data-stu-id="5fecc-145">-Name</span></span>
<span data-ttu-id="5fecc-146">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5fecc-146">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-147">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5fecc-147">-NoWait</span></span>
<span data-ttu-id="5fecc-148">Führen Sie den Befehl asynchron aus.</span><span class="sxs-lookup"><span data-stu-id="5fecc-148">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-149">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="5fecc-149">-PublicAccess</span></span>
<span data-ttu-id="5fecc-150">Bestimmt den öffentlichen Zugriff.</span><span class="sxs-lookup"><span data-stu-id="5fecc-150">Determines the public access.</span></span>
<span data-ttu-id="5fecc-151">Geben Sie einzelne oder einen Bereich von IP-Adressen ein, der in die Liste zulässiger Ip-Adressen aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fecc-151">Enter single or range of IP addresses to be included in the allowed list of IPs.</span></span>
<span data-ttu-id="5fecc-152">IP-Adressbereiche müssen durch Bindestriche getrennt sein und dürfen keine Leerzeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5fecc-152">IP address ranges must be dash- separated and not contain any spaces.</span></span>
<span data-ttu-id="5fecc-153">Wenn Sie 0.0.0.0 angeben, kann der öffentliche Zugriff von allen ressourcen, die in Azure bereitgestellt werden, auf Ihren Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="5fecc-153">Specifying 0.0.0.0 allows public access from any resources deployed within Azure to access your server.</span></span>
<span data-ttu-id="5fecc-154">Wenn Sie keine IP-Adresse angeben, wird der Server im Modus für den öffentlichen Zugriff festgelegt, aber keine Firewallregel erstellt.</span><span class="sxs-lookup"><span data-stu-id="5fecc-154">Specifying no IP address sets the server in public access mode but does not create a firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fecc-155">-ResourceGroupName</span></span>
<span data-ttu-id="5fecc-156">Der Name der Ressourcengruppe, die die Ressource enthält. Sie können diesen Wert über die Azure Resource Manager-API oder das Portal abrufen.</span><span class="sxs-lookup"><span data-stu-id="5fecc-156">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-157">-Sku</span><span class="sxs-lookup"><span data-stu-id="5fecc-157">-Sku</span></span>
<span data-ttu-id="5fecc-158">Der Name der Sku , in der Regel, Ebene + Familie + Kerne, z. B. Standard_B1ms, Standard_D2ds_v4.</span><span class="sxs-lookup"><span data-stu-id="5fecc-158">The name of the sku, typically, tier + family + cores, e.g. Standard_B1ms, Standard_D2ds_v4.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-159">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="5fecc-159">-SkuTier</span></span>
<span data-ttu-id="5fecc-160">Computeebene des Servers.</span><span class="sxs-lookup"><span data-stu-id="5fecc-160">Compute tier of the server.</span></span>
<span data-ttu-id="5fecc-161">Akzeptierte Werte: Burstable, GeneralPurpose, Memory Optimized.</span><span class="sxs-lookup"><span data-stu-id="5fecc-161">Accepted values: Burstable, GeneralPurpose, Memory Optimized.</span></span>
<span data-ttu-id="5fecc-162">Standard: Burstable.</span><span class="sxs-lookup"><span data-stu-id="5fecc-162">Default: Burstable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-163">-StorageInMb</span><span class="sxs-lookup"><span data-stu-id="5fecc-163">-StorageInMb</span></span>
<span data-ttu-id="5fecc-164">Maximaler Speicherplatz, der für einen Server zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="5fecc-164">Max storage allowed for a server.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-165">-Subnetz</span><span class="sxs-lookup"><span data-stu-id="5fecc-165">-Subnet</span></span>
<span data-ttu-id="5fecc-166">Der Name oder die ID eines vorhandenen Subnetzes oder der Name eines neuen Subnetzes, das erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fecc-166">The Name or Id of an existing Subnet or name of a new one to create.</span></span>
<span data-ttu-id="5fecc-167">Beachten Sie, dass das Subnetz an Microsoft.DBforMySQL/flexibleServers delegiert wird.</span><span class="sxs-lookup"><span data-stu-id="5fecc-167">Please note that the subnet will be delegated to Microsoft.DBforMySQL/flexibleServers.</span></span>
<span data-ttu-id="5fecc-168">Nach der Delegierung kann dieses Subnetz nicht für andere Arten von Azure-Ressourcen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fecc-168">After delegation, this subnet cannot be used for any other type of Azure resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-169">-SubnetPrefix</span><span class="sxs-lookup"><span data-stu-id="5fecc-169">-SubnetPrefix</span></span>
<span data-ttu-id="5fecc-170">Das Subnetz-IP-Adresspräfix, das beim Erstellen eines neuen Vnets im CIDR-Format verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fecc-170">The subnet IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="5fecc-171">Der Standardwert ist 10.0.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="5fecc-171">Default value is 10.0.0.0/24.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5fecc-172">-SubscriptionId</span></span>
<span data-ttu-id="5fecc-173">Die Abonnement-ID, die ein Azure-Abonnement identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5fecc-173">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="5fecc-174">-Tag</span></span>
<span data-ttu-id="5fecc-175">Anwendungsspezifische Metadaten in Form von Schlüssel-Wert-Paaren.</span><span class="sxs-lookup"><span data-stu-id="5fecc-175">Application-specific metadata in the form of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-176">-Version</span><span class="sxs-lookup"><span data-stu-id="5fecc-176">-Version</span></span>
<span data-ttu-id="5fecc-177">Serverversion.</span><span class="sxs-lookup"><span data-stu-id="5fecc-177">Server version.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Support.ServerVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-178">-Vnet</span><span class="sxs-lookup"><span data-stu-id="5fecc-178">-Vnet</span></span>
<span data-ttu-id="5fecc-179">Der Name oder die ID eines vorhandenen virtuellen Netzwerks oder der Name eines neuen zu erstellende Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="5fecc-179">The Name or Id of an existing virtual network or name of a new one to create.</span></span>
<span data-ttu-id="5fecc-180">Der Name muss zwischen 2 und 64 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="5fecc-180">The name must be between 2 to 64 characters.</span></span>
<span data-ttu-id="5fecc-181">Der Name muss mit einem Buchstaben oder einer Zahl beginnen, mit einem Buchstaben, einer Zahl oder einem Unterstrich enden und darf nur Buchstaben, Zahlen, Unterstriche, Punkte oder Bindestriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="5fecc-181">The name must begin with a letter or number, end with a letter, number or underscore, and may contain only letters, numbers, underscores, periods, or hyphens.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-182">-VnetPrefix</span><span class="sxs-lookup"><span data-stu-id="5fecc-182">-VnetPrefix</span></span>
<span data-ttu-id="5fecc-183">Das Präfix für die IP-Adresse, das beim Erstellen eines neuen Vnets im CIDR-Format verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fecc-183">The IP address prefix to use when creating a new vnet in CIDR format.</span></span>
<span data-ttu-id="5fecc-184">Der Standardwert ist 10.0.0.0/16.</span><span class="sxs-lookup"><span data-stu-id="5fecc-184">Default value is 10.0.0.0/16.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-185">-Zone</span><span class="sxs-lookup"><span data-stu-id="5fecc-185">-Zone</span></span>
<span data-ttu-id="5fecc-186">Verfügbarkeitszone, in der die Ressource bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5fecc-186">Availability zone into which to provision the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-187">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5fecc-187">-Confirm</span></span>
<span data-ttu-id="5fecc-188">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5fecc-188">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fecc-189">-WhatIf</span></span>
<span data-ttu-id="5fecc-190">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5fecc-190">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fecc-191">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fecc-191">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5fecc-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fecc-192">CommonParameters</span></span>
<span data-ttu-id="5fecc-193">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fecc-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fecc-194">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fecc-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fecc-195">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5fecc-195">INPUTS</span></span>

## <span data-ttu-id="5fecc-196">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5fecc-196">OUTPUTS</span></span>

### <span data-ttu-id="5fecc-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5fecc-197">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="5fecc-198">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5fecc-198">NOTES</span></span>

<span data-ttu-id="5fecc-199">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5fecc-199">ALIASES</span></span>

## <span data-ttu-id="5fecc-200">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5fecc-200">RELATED LINKS</span></span>

