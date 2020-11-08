---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175514"
---
# <span data-ttu-id="6d541-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6d541-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="6d541-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6d541-102">SYNOPSIS</span></span>
<span data-ttu-id="6d541-103">Ruft verwaltete HSM-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="6d541-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="6d541-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d541-104">SYNTAX</span></span>

### <span data-ttu-id="6d541-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Standard)</span><span class="sxs-lookup"><span data-stu-id="6d541-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d541-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="6d541-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d541-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="6d541-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d541-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="6d541-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d541-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="6d541-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d541-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="6d541-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d541-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="6d541-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d541-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="6d541-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6d541-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="6d541-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d541-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d541-114">DESCRIPTION</span></span>
<span data-ttu-id="6d541-115">Das Cmdlet " **Get-AzManagedHsmKey** " ruft Azure Managed HSM-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="6d541-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="6d541-116">Dieses Cmdlet ruft ein bestimmtes **Microsoft. Azure. Commands. keyvault. Models. keybundle** oder eine Liste aller **keybundle** -Objekte in einem verwalteten HSM oder einer Version ab.</span><span class="sxs-lookup"><span data-stu-id="6d541-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="6d541-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6d541-117">EXAMPLES</span></span>

### <span data-ttu-id="6d541-118">Beispiel 1: Abrufen aller Schlüssel in einem verwalteten HSM</span><span class="sxs-lookup"><span data-stu-id="6d541-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="6d541-119">Vault/HSM-Name: testmhsm Name: testkey001 Version: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey001 aktiviert: true läuft ab: nicht vorher: erstellt: 10/14/2020 3:39:16 am aktualisiert: 10/14/2020 3:39:16 am Wiederherstellungs Stufe: wiederherstellbare + bereinigende Tags:</span><span class="sxs-lookup"><span data-stu-id="6d541-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="6d541-120">Vault/HSM-Name: testmhsm Name: testkey002 Version: ID: https://testmhsm.managedhsm.azure.net:443/keys/testkey002 aktiviert: false läuft ab: 10/14/2022 8:13:29 am nicht vorher: 10/14/2020 8:13:33 am erstellt: 10/14/2020 8:14:01 Uhr aktualisiert: 10/14/2020 8:14:01 am Wiederherstellungs Stufe: wiederherstellbare + purgeable-Tags: Name-Wert-Schweregrad hohe Buchhaltung true</span><span class="sxs-lookup"><span data-stu-id="6d541-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="6d541-121">Dieser Befehl ruft alle Schlüssel im verwalteten HSM mit dem Namen testmhsm ab.</span><span class="sxs-lookup"><span data-stu-id="6d541-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="6d541-122">Beispiel 2: Abrufen der aktuellen Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="6d541-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="6d541-123">Dieser Befehl ruft die aktuelle Version des Schlüssels mit dem Namen testkey001 im verwalteten HSM mit dem Namen testmhsm ab.</span><span class="sxs-lookup"><span data-stu-id="6d541-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="6d541-124">Hinweis: der HSM-Name kann über $HSM abgerufen werden. Vaultname</span><span class="sxs-lookup"><span data-stu-id="6d541-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="6d541-125">Beispiel 3: Abrufen aller Versionen eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="6d541-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="6d541-126">Dieser Befehl ruft alle Versionen ab, die den Schlüssel mit dem Namen testkey001 im verwalteten HSM mit dem Namen testmhsm.</span><span class="sxs-lookup"><span data-stu-id="6d541-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="6d541-127">Beispiel 4: Abrufen einer bestimmten Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="6d541-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="6d541-128">Dieser Befehl ruft eine bestimmte Version des Schlüssels mit dem Namen TestKey im verwalteten HSM mit dem Namen testmhsm ab.</span><span class="sxs-lookup"><span data-stu-id="6d541-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="6d541-129">Nachdem Sie diesen Befehl ausgeführt haben, können Sie verschiedene Eigenschaften des Schlüssels überprüfen, indem Sie im $Key-Objekt navigieren.</span><span class="sxs-lookup"><span data-stu-id="6d541-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="6d541-130">Beispiel 5: Abrufen aller Schlüssel, die gelöscht, aber nicht für dieses verwaltete HSM bereinigt wurden</span><span class="sxs-lookup"><span data-stu-id="6d541-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="6d541-131">Dieser Befehl ruft alle Schlüssel ab, die zuvor gelöscht, aber nicht bereinigt wurden, im verwalteten HSM mit dem Namen testmhsm.</span><span class="sxs-lookup"><span data-stu-id="6d541-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="6d541-132">Beispiel 6: Ruft den Schlüssel TestKey ab, der gelöscht, aber nicht bereinigt wurde, für dieses verwaltete HSM</span><span class="sxs-lookup"><span data-stu-id="6d541-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="6d541-133">Dieser Befehl ruft den Schlüssel TestKey ab, der zuvor gelöscht, aber nicht bereinigt wurde, im verwalteten HSM mit dem Namen testmhsm.</span><span class="sxs-lookup"><span data-stu-id="6d541-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="6d541-134">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="6d541-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="6d541-135">Beispiel 7: Abrufen aller Schlüssel in einem verwalteten HSM mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="6d541-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="6d541-136">Dieser Befehl ruft alle Schlüssel im verwalteten HSM mit dem Namen "testmhsm" ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="6d541-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="6d541-137">Beispiel 8: Herunterladen eines öffentlichen Schlüssels als PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="6d541-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="6d541-138">Sie können den öffentlichen Schlüssel eines RSA-Schlüssels herunterladen, indem Sie den `-OutFile` Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="6d541-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="6d541-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="6d541-139">PARAMETERS</span></span>

### <span data-ttu-id="6d541-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d541-140">-DefaultProfile</span></span>
<span data-ttu-id="6d541-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6d541-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d541-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="6d541-142">-HsmName</span></span>
<span data-ttu-id="6d541-143">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="6d541-143">HSM name.</span></span> <span data-ttu-id="6d541-144">Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="6d541-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d541-145">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="6d541-145">-IncludeVersions</span></span>
<span data-ttu-id="6d541-146">Gibt an, ob die Versionen des Schlüssels in die Ausgabe eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d541-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d541-147">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6d541-147">-InputObject</span></span>
<span data-ttu-id="6d541-148">HSM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6d541-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d541-149">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="6d541-149">-InRemovedState</span></span>
<span data-ttu-id="6d541-150">Gibt an, ob die zuvor gelöschten Schlüssel in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6d541-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d541-151">-Name</span><span class="sxs-lookup"><span data-stu-id="6d541-151">-Name</span></span>
<span data-ttu-id="6d541-152">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="6d541-152">Key name.</span></span>
<span data-ttu-id="6d541-153">Cmdlet erstellt den FQDN eines Schlüssels aus verwaltetem HSM-Namen, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="6d541-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d541-154">-Datei</span><span class="sxs-lookup"><span data-stu-id="6d541-154">-OutFile</span></span>
<span data-ttu-id="6d541-155">Gibt die Ausgabedatei an, für die dieses Cmdlet den Schlüssel speichert.</span><span class="sxs-lookup"><span data-stu-id="6d541-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="6d541-156">Der öffentliche Schlüssel wird standardmäßig im PEM-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6d541-156">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="6d541-157">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6d541-157">-ResourceId</span></span>
<span data-ttu-id="6d541-158">HSM-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6d541-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d541-159">-Version</span><span class="sxs-lookup"><span data-stu-id="6d541-159">-Version</span></span>
<span data-ttu-id="6d541-160">Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="6d541-160">Key version.</span></span>
<span data-ttu-id="6d541-161">Cmdlet erstellt den FQDN eines Schlüssels aus verwaltetem HSM-Namen, aktuell ausgewählter Umgebung, Schlüsselname und Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="6d541-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d541-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d541-162">CommonParameters</span></span>
<span data-ttu-id="6d541-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d541-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d541-164">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d541-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d541-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6d541-165">INPUTS</span></span>

### <span data-ttu-id="6d541-166">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6d541-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="6d541-167">System. String</span><span class="sxs-lookup"><span data-stu-id="6d541-167">System.String</span></span>

## <span data-ttu-id="6d541-168">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6d541-168">OUTPUTS</span></span>

### <span data-ttu-id="6d541-169">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6d541-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="6d541-170">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6d541-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="6d541-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6d541-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="6d541-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6d541-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="6d541-173">Notizen</span><span class="sxs-lookup"><span data-stu-id="6d541-173">NOTES</span></span>

## <span data-ttu-id="6d541-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6d541-174">RELATED LINKS</span></span>

[<span data-ttu-id="6d541-175">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6d541-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="6d541-176">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6d541-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="6d541-177">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6d541-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="6d541-178">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="6d541-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="6d541-179">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6d541-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="6d541-180">Wiederherstellen – AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="6d541-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)