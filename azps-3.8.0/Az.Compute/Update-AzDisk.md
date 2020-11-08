---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: 662ea1355cfa687f9fc34b95ec71a430ae287f41
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003633"
---
# <span data-ttu-id="e103d-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="e103d-101">Update-AzDisk</span></span>

## <span data-ttu-id="e103d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e103d-102">SYNOPSIS</span></span>
<span data-ttu-id="e103d-103">Aktualisiert einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="e103d-103">Updates a disk.</span></span>

## <span data-ttu-id="e103d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e103d-104">SYNTAX</span></span>

### <span data-ttu-id="e103d-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="e103d-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e103d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="e103d-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e103d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e103d-107">DESCRIPTION</span></span>
<span data-ttu-id="e103d-108">Das Cmdlet **Update-AzDisk** aktualisiert einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="e103d-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="e103d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e103d-109">EXAMPLES</span></span>

### <span data-ttu-id="e103d-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e103d-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="e103d-111">Der erste Befehl erstellt ein lokales leeres Datenträger Aktualisierungs Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="e103d-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e103d-112">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e103d-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e103d-113">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="e103d-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="e103d-114">Der letzte Befehl übernimmt das Datenträger Aktualisierungs Objekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e103d-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="e103d-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e103d-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="e103d-116">Mit diesem Befehl wird ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e103d-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="e103d-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="e103d-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="e103d-118">Diese Befehle aktualisieren auch einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße.</span><span class="sxs-lookup"><span data-stu-id="e103d-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="e103d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="e103d-119">PARAMETERS</span></span>

### <span data-ttu-id="e103d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e103d-120">-AsJob</span></span>
<span data-ttu-id="e103d-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="e103d-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e103d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e103d-122">-DefaultProfile</span></span>
<span data-ttu-id="e103d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e103d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e103d-124">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="e103d-124">-Disk</span></span>
<span data-ttu-id="e103d-125">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="e103d-125">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e103d-126">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="e103d-126">-DiskName</span></span>
<span data-ttu-id="e103d-127">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="e103d-127">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e103d-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e103d-128">-DiskUpdate</span></span>
<span data-ttu-id="e103d-129">Gibt ein lokales Datenträger Aktualisierungs Objekt an.</span><span class="sxs-lookup"><span data-stu-id="e103d-129">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e103d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e103d-130">-ResourceGroupName</span></span>
<span data-ttu-id="e103d-131">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="e103d-131">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e103d-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e103d-132">-Confirm</span></span>
<span data-ttu-id="e103d-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e103d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e103d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e103d-134">-WhatIf</span></span>
<span data-ttu-id="e103d-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e103d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e103d-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e103d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e103d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e103d-137">CommonParameters</span></span>
<span data-ttu-id="e103d-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e103d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e103d-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e103d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e103d-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e103d-140">INPUTS</span></span>

### <span data-ttu-id="e103d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e103d-141">System.String</span></span>

### <span data-ttu-id="e103d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="e103d-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="e103d-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="e103d-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e103d-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e103d-144">OUTPUTS</span></span>

### <span data-ttu-id="e103d-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="e103d-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e103d-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="e103d-146">NOTES</span></span>

## <span data-ttu-id="e103d-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e103d-147">RELATED LINKS</span></span>
