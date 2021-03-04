---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzDisk.md
ms.openlocfilehash: c8ab3583fed5c65468bccf5282b5fae44a4a5c20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947507"
---
# <span data-ttu-id="055fb-101">Update-AzDisk</span><span class="sxs-lookup"><span data-stu-id="055fb-101">Update-AzDisk</span></span>

## <span data-ttu-id="055fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="055fb-102">SYNOPSIS</span></span>
<span data-ttu-id="055fb-103">Aktualisiert einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="055fb-103">Updates a disk.</span></span>

## <span data-ttu-id="055fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="055fb-104">SYNTAX</span></span>

### <span data-ttu-id="055fb-105">Standardparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="055fb-105">DefaultParameter (Default)</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="055fb-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="055fb-106">FriendMethod</span></span>
```
Update-AzDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="055fb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="055fb-107">DESCRIPTION</span></span>
<span data-ttu-id="055fb-108">Das **Update-AzDisk-Cmdlet** aktualisiert einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="055fb-108">The **Update-AzDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="055fb-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="055fb-109">EXAMPLES</span></span>

### <span data-ttu-id="055fb-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="055fb-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="055fb-111">Mit dem ersten Befehl wird ein lokales leeres Datenträgeraktualisierungsobjekt mit der Größe 10 GB in Premium_LRS Speicherkontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="055fb-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="055fb-112">Außerdem wird der Windows -Betriebssystemtyp festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="055fb-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="055fb-113">Mit dem zweiten und dritten Befehl werden die Einstellungen für den Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüssel für das Datenträgeraktualisierungsobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="055fb-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="055fb-114">Der letzte Befehl übernimmt das Datenträgeraktualisierungsobjekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="055fb-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="055fb-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="055fb-115">Example 2</span></span>
```
PS C:\> New-AzDiskUpdateConfig -DiskSizeGB 10 | Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="055fb-116">Mit diesem Befehl wird ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf eine Datenträgergröße von 10 GB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="055fb-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="055fb-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="055fb-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="055fb-118">Mit diesen Befehlen wird auch ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf eine Datenträgergröße von 10 GB aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="055fb-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="055fb-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="055fb-119">PARAMETERS</span></span>

### <span data-ttu-id="055fb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="055fb-120">-AsJob</span></span>
<span data-ttu-id="055fb-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zurück, um den Fortschritt zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="055fb-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="055fb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="055fb-122">-DefaultProfile</span></span>
<span data-ttu-id="055fb-123">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="055fb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="055fb-124">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="055fb-124">-Disk</span></span>
<span data-ttu-id="055fb-125">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="055fb-125">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="055fb-126">-DiskName</span><span class="sxs-lookup"><span data-stu-id="055fb-126">-DiskName</span></span>
<span data-ttu-id="055fb-127">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="055fb-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="055fb-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="055fb-128">-DiskUpdate</span></span>
<span data-ttu-id="055fb-129">Gibt ein lokales Datenträgeraktualisierungsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="055fb-129">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="055fb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="055fb-130">-ResourceGroupName</span></span>
<span data-ttu-id="055fb-131">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="055fb-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="055fb-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="055fb-132">-Confirm</span></span>
<span data-ttu-id="055fb-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="055fb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="055fb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="055fb-134">-WhatIf</span></span>
<span data-ttu-id="055fb-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="055fb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="055fb-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="055fb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="055fb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="055fb-137">CommonParameters</span></span>
<span data-ttu-id="055fb-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="055fb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="055fb-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="055fb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="055fb-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="055fb-140">INPUTS</span></span>

### <span data-ttu-id="055fb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="055fb-141">System.String</span></span>

### <span data-ttu-id="055fb-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="055fb-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="055fb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="055fb-143">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="055fb-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="055fb-144">OUTPUTS</span></span>

### <span data-ttu-id="055fb-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="055fb-145">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="055fb-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="055fb-146">NOTES</span></span>

## <span data-ttu-id="055fb-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="055fb-147">RELATED LINKS</span></span>
