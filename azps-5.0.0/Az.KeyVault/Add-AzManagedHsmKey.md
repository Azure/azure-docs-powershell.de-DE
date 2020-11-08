---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180439"
---
# <span data-ttu-id="61dff-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="61dff-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="61dff-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61dff-102">SYNOPSIS</span></span>
<span data-ttu-id="61dff-103">Erstellt einen Schlüssel in einem verwalteten HSM oder importiert einen Schlüssel in ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="61dff-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="61dff-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61dff-104">SYNTAX</span></span>

### <span data-ttu-id="61dff-105">InteractiveCreate (Standard)</span><span class="sxs-lookup"><span data-stu-id="61dff-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61dff-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="61dff-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61dff-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="61dff-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61dff-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="61dff-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61dff-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="61dff-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61dff-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="61dff-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="61dff-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61dff-111">DESCRIPTION</span></span>
<span data-ttu-id="61dff-112">Das Cmdlet **Add-AzManagedHsmKey** erstellt einen Schlüssel in einem verwalteten HSM in Azure Managed HSM oder importiert einen Schlüssel in ein verwaltetes HSM.</span><span class="sxs-lookup"><span data-stu-id="61dff-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="61dff-113">Verwenden Sie dieses Cmdlet, um Schlüssel mithilfe einer der folgenden Methoden hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="61dff-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="61dff-114">Erstellen eines Schlüssels mit Standardschlüssel Attributen</span><span class="sxs-lookup"><span data-stu-id="61dff-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="61dff-115">Erstellen eines Schlüssels mit angegebenen Schlüsselattributen</span><span class="sxs-lookup"><span data-stu-id="61dff-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="61dff-116">Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="61dff-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="61dff-117">Für alle diese Vorgänge können Sie wichtige Attribute bereitstellen oder Standardeinstellungen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="61dff-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="61dff-118">Wenn Sie einen Schlüssel erstellen oder importieren, der denselben Namen wie ein vorhandener Schlüssel in Ihrem verwalteten HSM hat, wird der ursprüngliche Schlüssel mit den Werten aktualisiert, die Sie für den neuen Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="61dff-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="61dff-119">Sie können mithilfe des versionsspezifischen URIs für diese Version des Schlüssels auf die vorherigen Werte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="61dff-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="61dff-120">Informationen zu Schlüssel Versionen und der URI-Struktur finden Sie unter [Informationen zu Schlüsseln und Geheimnissen](http://go.microsoft.com/fwlink/?linkid=518560) in der Managed HSM-Dokumentation zur Ruhezeit-API.</span><span class="sxs-lookup"><span data-stu-id="61dff-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="61dff-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61dff-121">EXAMPLES</span></span>

### <span data-ttu-id="61dff-122">Beispiel 1: Erstellen eines RSA-HSM-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="61dff-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="61dff-123">Dieser Befehl erstellt einen RSA-HSM-Schlüssel mit dem Namen TestKey im verwalteten HSM-TestKey mit dem Namen testmhsm.</span><span class="sxs-lookup"><span data-stu-id="61dff-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="61dff-124">Beispiel 2: Erstellen eines EC-HSM-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="61dff-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="61dff-125">Dieser Befehl erstellt einen EC-HSM-Schlüssel mit dem Namen TestKey mit P-256-Kurve im verwalteten HSM-TestKey mit dem Namen testmhsm.</span><span class="sxs-lookup"><span data-stu-id="61dff-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="61dff-126">Beispiel 3: Erstellen eines OAT-HSM-Schlüssels mit nicht standardmäßigen Werten</span><span class="sxs-lookup"><span data-stu-id="61dff-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
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

<span data-ttu-id="61dff-127">Der erste Befehl speichert die Werte, die entschlüsselt und in der $KeyOperations Variablen überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="61dff-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="61dff-128">Mit dem zweiten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt, das in UTC definiert ist.</span><span class="sxs-lookup"><span data-stu-id="61dff-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="61dff-129">Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an.</span><span class="sxs-lookup"><span data-stu-id="61dff-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="61dff-130">Der Befehl speichert dieses Datum in der $Expires Variablen.</span><span class="sxs-lookup"><span data-stu-id="61dff-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="61dff-131">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="61dff-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="61dff-132">Der dritte Befehl erstellt mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="61dff-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="61dff-133">Dieses Objekt gibt die aktuelle UTC-Zeit an.</span><span class="sxs-lookup"><span data-stu-id="61dff-133">That object specifies current UTC time.</span></span> <span data-ttu-id="61dff-134">Der Befehl speichert dieses Datum in der $NotBefore Variablen.</span><span class="sxs-lookup"><span data-stu-id="61dff-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="61dff-135">Der endgültige Befehl erstellt einen Schlüssel mit dem Namen TestKey, bei dem es sich um einen OAT-HSM-Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="61dff-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="61dff-136">Der Befehl gibt Werte für zulässige Schlüsselvorgänge an, die $KeyOperations gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="61dff-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="61dff-137">Der Befehl gibt die Zeiten für die in den vorherigen Befehlen erstellten Ablauf-und *NotBefore* -Parameter sowie die Tags für den höchsten Schweregrad und das *Datum* an.</span><span class="sxs-lookup"><span data-stu-id="61dff-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="61dff-138">Der neue Schlüssel ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="61dff-138">The new key is disabled.</span></span> <span data-ttu-id="61dff-139">Sie können es mithilfe des Cmdlets **Update-AzManagedHsmKey** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="61dff-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="61dff-140">Parameter</span><span class="sxs-lookup"><span data-stu-id="61dff-140">PARAMETERS</span></span>

### <span data-ttu-id="61dff-141">-Curvename</span><span class="sxs-lookup"><span data-stu-id="61dff-141">-CurveName</span></span>
<span data-ttu-id="61dff-142">Gibt den Kurven Namen der elliptischen Kurven Kryptographie an, dieser Wert ist gültig, wenn KeyType EC ist.</span><span class="sxs-lookup"><span data-stu-id="61dff-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

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

### <span data-ttu-id="61dff-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61dff-143">-DefaultProfile</span></span>
<span data-ttu-id="61dff-144">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61dff-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61dff-145">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="61dff-145">-Disable</span></span>
<span data-ttu-id="61dff-146">Gibt an, dass der hinzuzufügende Schlüssel auf den Anfangszustand disabled festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="61dff-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="61dff-147">Jeder Versuch, den Schlüssel zu verwenden, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="61dff-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="61dff-148">Verwenden Sie diesen Parameter, wenn Sie Schlüssel Vorabladen, die Sie später aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="61dff-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="61dff-149">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="61dff-149">-Expires</span></span>
<span data-ttu-id="61dff-150">Gibt die Ablaufzeit des Schlüssels in UTC an.</span><span class="sxs-lookup"><span data-stu-id="61dff-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="61dff-151">Wenn keine Angabe erfolgt, läuft Key nicht ab.</span><span class="sxs-lookup"><span data-stu-id="61dff-151">If not specified, key will not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="61dff-152">-HsmName</span></span>
<span data-ttu-id="61dff-153">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="61dff-153">HSM name.</span></span> <span data-ttu-id="61dff-154">Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="61dff-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-155">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="61dff-155">-InputObject</span></span>
<span data-ttu-id="61dff-156">HSM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="61dff-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-157">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="61dff-157">-KeyFilePassword</span></span>
<span data-ttu-id="61dff-158">Kennwort der lokalen Datei mit dem Schlüsselmaterial, das importiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="61dff-158">Password of the local file containing the key material to be imported.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-159">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="61dff-159">-KeyFilePath</span></span>
<span data-ttu-id="61dff-160">Der Pfad zu der lokalen Datei, die das zu importierende Schlüsselmaterial enthält.</span><span class="sxs-lookup"><span data-stu-id="61dff-160">Path to the local file containing the key material to be imported.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-161">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="61dff-161">-KeyOps</span></span>
<span data-ttu-id="61dff-162">Die Vorgänge, die mit dem Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="61dff-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="61dff-163">Wenn diese nicht vorhanden sind, können alle Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="61dff-163">If not present, all operations can be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-164">-KeyType</span><span class="sxs-lookup"><span data-stu-id="61dff-164">-KeyType</span></span>
<span data-ttu-id="61dff-165">Gibt den Schlüsseltyp dieses Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="61dff-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-166">-Name</span><span class="sxs-lookup"><span data-stu-id="61dff-166">-Name</span></span>
<span data-ttu-id="61dff-167">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="61dff-167">Key name.</span></span>
<span data-ttu-id="61dff-168">Cmdlet erstellt den FQDN eines Schlüssels aus verwaltetem HSM-Namen, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="61dff-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-169">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="61dff-169">-NotBefore</span></span>
<span data-ttu-id="61dff-170">Die UTC-Zeit, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="61dff-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="61dff-171">Wenn keine Angabe erfolgt, gibt es keine Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="61dff-171">If not specified, there is no limitation.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-172">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="61dff-172">-ResourceId</span></span>
<span data-ttu-id="61dff-173">HSM-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="61dff-173">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-174">-Size</span><span class="sxs-lookup"><span data-stu-id="61dff-174">-Size</span></span>
<span data-ttu-id="61dff-175">RSA-Schlüsselgröße in Bits.</span><span class="sxs-lookup"><span data-stu-id="61dff-175">RSA key size, in bits.</span></span>
<span data-ttu-id="61dff-176">Wenn keine Angabe erfolgt, stellt der Dienst einen sicheren Standard bereit.</span><span class="sxs-lookup"><span data-stu-id="61dff-176">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-177">-Tag</span><span class="sxs-lookup"><span data-stu-id="61dff-177">-Tag</span></span>
<span data-ttu-id="61dff-178">Eine Hashtable, die Schlüsselkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="61dff-178">A hashtable representing key tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61dff-179">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="61dff-179">-Confirm</span></span>
<span data-ttu-id="61dff-180">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="61dff-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61dff-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61dff-181">-WhatIf</span></span>
<span data-ttu-id="61dff-182">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61dff-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61dff-183">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="61dff-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61dff-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61dff-184">CommonParameters</span></span>
<span data-ttu-id="61dff-185">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61dff-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61dff-186">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61dff-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61dff-187">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61dff-187">INPUTS</span></span>

### <span data-ttu-id="61dff-188">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="61dff-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="61dff-189">System. String</span><span class="sxs-lookup"><span data-stu-id="61dff-189">System.String</span></span>

## <span data-ttu-id="61dff-190">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61dff-190">OUTPUTS</span></span>

### <span data-ttu-id="61dff-191">Microsoft. Azure. Commands. keyvault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="61dff-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="61dff-192">Notizen</span><span class="sxs-lookup"><span data-stu-id="61dff-192">NOTES</span></span>

## <span data-ttu-id="61dff-193">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61dff-193">RELATED LINKS</span></span>

[<span data-ttu-id="61dff-194">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="61dff-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="61dff-195">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="61dff-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="61dff-196">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="61dff-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="61dff-197">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="61dff-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="61dff-198">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="61dff-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="61dff-199">Wiederherstellen – AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="61dff-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
