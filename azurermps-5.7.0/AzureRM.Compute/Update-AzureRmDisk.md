---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmDisk.md
ms.openlocfilehash: 30a6ac1a3d74423302cc8b39e8b494e2f1ee2e22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662234"
---
# <span data-ttu-id="f7f8a-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="f7f8a-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="f7f8a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f8a-103">Aktualisiert einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7f8a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7f8a-104">SYNTAX</span></span>

### <span data-ttu-id="f7f8a-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7f8a-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <DiskUpdate> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f8a-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f7f8a-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <Disk> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7f8a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7f8a-107">DESCRIPTION</span></span>
<span data-ttu-id="f7f8a-108">Das Cmdlet **Update-AzureRmDisk** aktualisiert einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="f7f8a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7f8a-109">EXAMPLES</span></span>

### <span data-ttu-id="f7f8a-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7f8a-110">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="f7f8a-111">Der erste Befehl erstellt ein lokales leeres Datenträger Aktualisierungs Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="f7f8a-112">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="f7f8a-113">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="f7f8a-114">Der letzte Befehl übernimmt das Datenträger Aktualisierungs Objekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="f7f8a-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="f7f8a-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f7f8a-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="f7f8a-116">Mit diesem Befehl wird ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="f7f8a-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f7f8a-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="f7f8a-118">Diese Befehle aktualisieren auch einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="f7f8a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7f8a-119">PARAMETERS</span></span>

### <span data-ttu-id="f7f8a-120">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="f7f8a-120">-Disk</span></span>
<span data-ttu-id="f7f8a-121">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-121">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f8a-122">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="f7f8a-122">-DiskName</span></span>
<span data-ttu-id="f7f8a-123">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-123">Specifies the name of a disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f8a-124">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="f7f8a-124">-DiskUpdate</span></span>
<span data-ttu-id="f7f8a-125">Gibt ein lokales Datenträger Aktualisierungs Objekt an.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-125">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f8a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f8a-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7f8a-127">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-127">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f8a-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7f8a-128">-Confirm</span></span>
<span data-ttu-id="f7f8a-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f8a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f8a-130">-WhatIf</span></span>
<span data-ttu-id="f7f8a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f8a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7f8a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f8a-133">CommonParameters</span></span>
<span data-ttu-id="f7f8a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f8a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f8a-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f8a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f8a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7f8a-136">INPUTS</span></span>

### <span data-ttu-id="f7f8a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f7f8a-137">System.String</span></span>
<span data-ttu-id="f7f8a-138">Microsoft. Azure. Management. Compute. Models. DiskUpdate Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="f7f8a-138">Microsoft.Azure.Management.Compute.Models.DiskUpdate Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="f7f8a-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7f8a-139">OUTPUTS</span></span>

### <span data-ttu-id="f7f8a-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="f7f8a-140">System.Object</span></span>

## <span data-ttu-id="f7f8a-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7f8a-141">NOTES</span></span>

## <span data-ttu-id="f7f8a-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7f8a-142">RELATED LINKS</span></span>

