---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermdisk
schema: 2.0.0
ms.openlocfilehash: 06cd8d41fcdaaed6a05f7f7a137cbf75542be62b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850867"
---
# <span data-ttu-id="2c5ee-101">Update-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="2c5ee-101">Update-AzureRmDisk</span></span>

## <span data-ttu-id="2c5ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c5ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5ee-103">Aktualisiert einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-103">Updates a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c5ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c5ee-104">SYNTAX</span></span>

### <span data-ttu-id="2c5ee-105">Defaultparameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="2c5ee-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-DiskUpdate] <PSDiskUpdate> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c5ee-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="2c5ee-106">FriendMethod</span></span>
```
Update-AzureRmDisk [-ResourceGroupName] <String> [-DiskName] <String> [-Disk] <PSDisk> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c5ee-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c5ee-107">DESCRIPTION</span></span>
<span data-ttu-id="2c5ee-108">Das Cmdlet **Update-AzureRmDisk** aktualisiert einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-108">The **Update-AzureRmDisk** cmdlet updates a disk.</span></span>

## <span data-ttu-id="2c5ee-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c5ee-109">EXAMPLES</span></span>

### <span data-ttu-id="2c5ee-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c5ee-110">Example 1</span></span>
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

<span data-ttu-id="2c5ee-111">Der erste Befehl erstellt ein lokales leeres Datenträger Aktualisierungs Objekt mit der Größe 10 GB in Premium_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-111">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="2c5ee-112">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-112">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="2c5ee-113">Der zweite und der dritte Befehl legen die Einstellungen für den Datenträgerverschlüsselungsschlüssel und den Schlüssel Verschlüsselungsschlüssel für das Datenträger Aktualisierungs Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-113">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="2c5ee-114">Der letzte Befehl übernimmt das Datenträger Aktualisierungs Objekt und aktualisiert einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="2c5ee-114">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="2c5ee-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2c5ee-115">Example 2</span></span>
```
PS C:\> New-AzureRmDiskUpdateConfig -DiskSizeGB 10 | Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
```

<span data-ttu-id="2c5ee-116">Mit diesem Befehl wird ein vorhandener Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-116">This command updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

### <span data-ttu-id="2c5ee-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="2c5ee-117">Example 3</span></span>
```
PS C:\> $disk = Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01';
PS C:\> $disk.DiskSizeGB = 10;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $disk;
```

<span data-ttu-id="2c5ee-118">Diese Befehle aktualisieren auch einen vorhandenen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01" auf 10 GB Festplattengröße.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-118">These commands also update an existing disk with name 'Disk01' in resource group 'ResourceGroup01' to 10 GB disk size.</span></span>

## <span data-ttu-id="2c5ee-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c5ee-119">PARAMETERS</span></span>

### <span data-ttu-id="2c5ee-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c5ee-120">-AsJob</span></span>
<span data-ttu-id="2c5ee-121">Führen Sie das Cmdlet im Hintergrund aus, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c5ee-122">-DefaultProfile</span></span>
<span data-ttu-id="2c5ee-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c5ee-124">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="2c5ee-124">-Disk</span></span>
<span data-ttu-id="2c5ee-125">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-125">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c5ee-126">-Daten Trägername</span><span class="sxs-lookup"><span data-stu-id="2c5ee-126">-DiskName</span></span>
<span data-ttu-id="2c5ee-127">Gibt den Namen eines Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-127">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="2c5ee-128">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="2c5ee-128">-DiskUpdate</span></span>
<span data-ttu-id="2c5ee-129">Gibt ein lokales Datenträger Aktualisierungs Objekt an.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-129">Specifies a local disk update object.</span></span>

```yaml
Type: PSDiskUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c5ee-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c5ee-130">-ResourceGroupName</span></span>
<span data-ttu-id="2c5ee-131">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-131">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2c5ee-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2c5ee-132">-Confirm</span></span>
<span data-ttu-id="2c5ee-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c5ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c5ee-134">-WhatIf</span></span>
<span data-ttu-id="2c5ee-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c5ee-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c5ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5ee-137">CommonParameters</span></span>
<span data-ttu-id="2c5ee-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c5ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5ee-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c5ee-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5ee-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c5ee-140">INPUTS</span></span>

### <span data-ttu-id="2c5ee-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2c5ee-141">System.String</span></span>
<span data-ttu-id="2c5ee-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="2c5ee-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="2c5ee-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c5ee-143">OUTPUTS</span></span>

### <span data-ttu-id="2c5ee-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIsk</span><span class="sxs-lookup"><span data-stu-id="2c5ee-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="2c5ee-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c5ee-145">NOTES</span></span>

## <span data-ttu-id="2c5ee-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c5ee-146">RELATED LINKS</span></span>

