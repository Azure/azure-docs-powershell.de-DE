---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: cbbe321f23fb95bca8a4a70dd59f30ec098cf2d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948619"
---
# <span data-ttu-id="5ac6e-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="5ac6e-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="5ac6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ac6e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac6e-103">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-103">Gets information about a server.</span></span>

## <span data-ttu-id="5ac6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ac6e-104">SYNTAX</span></span>

### <span data-ttu-id="5ac6e-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ac6e-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ac6e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5ac6e-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ac6e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ac6e-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5ac6e-108">Liste</span><span class="sxs-lookup"><span data-stu-id="5ac6e-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5ac6e-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ac6e-109">DESCRIPTION</span></span>
<span data-ttu-id="5ac6e-110">Ruft Informationen zu einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-110">Gets information about a server.</span></span>

## <span data-ttu-id="5ac6e-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5ac6e-111">EXAMPLES</span></span>

### <span data-ttu-id="5ac6e-112">Beispiel 1: Get MySql server with default context</span><span class="sxs-lookup"><span data-stu-id="5ac6e-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="5ac6e-113">Dieses Cmdlet ruft MySql-Server mit Standardkontext ab.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="5ac6e-114">Beispiel 2: Get MySql server by resource group and server name</span><span class="sxs-lookup"><span data-stu-id="5ac6e-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="5ac6e-115">Dieses Cmdlet ruft MySql-Server nach Ressourcengruppe und Servernamen ab.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="5ac6e-116">Beispiel 3: Listet alle MySql-Server in einer angegebenen Ressourcengruppe auf.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="5ac6e-117">In diesem Cmdlet werden alle MySql-Server in der angegebenen Ressourcengruppe aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="5ac6e-118">Beispiel 4: Holen Sie sich den MySql-Server nach Identität</span><span class="sxs-lookup"><span data-stu-id="5ac6e-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="5ac6e-119">Diese Cmdletlisten ruft MySql-Server nach Identität ab.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="5ac6e-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5ac6e-120">PARAMETERS</span></span>

### <span data-ttu-id="5ac6e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ac6e-121">-DefaultProfile</span></span>
<span data-ttu-id="5ac6e-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ac6e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ac6e-123">-InputObject</span></span>
<span data-ttu-id="5ac6e-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ac6e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="5ac6e-125">-Name</span></span>
<span data-ttu-id="5ac6e-126">Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-126">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac6e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ac6e-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ac6e-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-128">The name of the resource group.</span></span>
<span data-ttu-id="5ac6e-129">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac6e-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5ac6e-130">-SubscriptionId</span></span>
<span data-ttu-id="5ac6e-131">Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ac6e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac6e-132">CommonParameters</span></span>
<span data-ttu-id="5ac6e-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac6e-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ac6e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac6e-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5ac6e-135">INPUTS</span></span>

### <span data-ttu-id="5ac6e-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="5ac6e-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="5ac6e-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5ac6e-137">OUTPUTS</span></span>

### <span data-ttu-id="5ac6e-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="5ac6e-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="5ac6e-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5ac6e-139">NOTES</span></span>

<span data-ttu-id="5ac6e-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="5ac6e-140">ALIASES</span></span>

<span data-ttu-id="5ac6e-141">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="5ac6e-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5ac6e-142">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ac6e-143">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5ac6e-144">INPUTOBJECT <IMySqlIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="5ac6e-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ac6e-145">`[ConfigurationName <String>]`: Der Name der Serverkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5ac6e-146">`[DatabaseName <String>]`: Der Name der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5ac6e-147">`[FirewallRuleName <String>]`: Der Name der Serverfirewallregel.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5ac6e-148">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="5ac6e-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ac6e-149">`[KeyName <String>]`: Der Name des Serverschlüssels.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="5ac6e-150">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5ac6e-151">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5ac6e-152">Der Name ist groß- und kleinschreibungsunabhängiger.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="5ac6e-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Der Name der Sicherheitsbenachrichtigungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5ac6e-154">`[ServerName <String>]`: Der Name des Servers.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5ac6e-155">`[SubscriptionId <String>]`: Die ID des Zielabonnements.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5ac6e-156">`[VirtualNetworkRuleName <String>]`: Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="5ac6e-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5ac6e-157">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5ac6e-157">RELATED LINKS</span></span>

