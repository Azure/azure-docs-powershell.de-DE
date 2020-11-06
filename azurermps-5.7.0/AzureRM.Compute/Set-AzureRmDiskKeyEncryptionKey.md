---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskKeyEncryptionKey.md
ms.openlocfilehash: bcefac746d643bfa64b28c623292e6473f8a4986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499010"
---
# <span data-ttu-id="420ea-101">Set-AzureRmDiskKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="420ea-101">Set-AzureRmDiskKeyEncryptionKey</span></span>

## <span data-ttu-id="420ea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="420ea-102">SYNOPSIS</span></span>
<span data-ttu-id="420ea-103">Legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="420ea-103">Sets the key encryption key properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="420ea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="420ea-104">SYNTAX</span></span>

```
Set-AzureRmDiskKeyEncryptionKey [-Disk] <Disk> [[-KeyUrl] <String>] [[-SourceVaultId] <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="420ea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="420ea-105">DESCRIPTION</span></span>
<span data-ttu-id="420ea-106">Das Cmdlet " **Set-AzureRmDiskKeyEncryptionKey** " legt die Key-Verschlüsselungsschlüssel Eigenschaften für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="420ea-106">The **Set-AzureRmDiskKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk object.</span></span>

## <span data-ttu-id="420ea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="420ea-107">EXAMPLES</span></span>

### <span data-ttu-id="420ea-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="420ea-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -Location 'Central US' -DiskSizeGB 5 -AccountType StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzureRmDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzureRmDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="420ea-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit der Größe 5 GB in Standard_LRS Speicher Kontotyp.</span><span class="sxs-lookup"><span data-stu-id="420ea-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="420ea-110">Darüber hinaus wird der Windows-Betriebssystemtyp festgelegt und die Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="420ea-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="420ea-111">Der zweite und der dritte Befehl legen den Datenträgerverschlüsselungsschlüssel und die Schlüsseleinstellungen für den Verschlüsselungsschlüssel für das Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="420ea-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="420ea-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="420ea-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="420ea-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="420ea-113">PARAMETERS</span></span>

### <span data-ttu-id="420ea-114">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="420ea-114">-Disk</span></span>
<span data-ttu-id="420ea-115">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="420ea-115">Specifies a local disk object.</span></span>

```yaml
Type: Disk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="420ea-116">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="420ea-116">-KeyUrl</span></span>
<span data-ttu-id="420ea-117">Gibt an die Schlüssel-URL.</span><span class="sxs-lookup"><span data-stu-id="420ea-117">Specifes the key Url.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420ea-118">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="420ea-118">-SourceVaultId</span></span>
<span data-ttu-id="420ea-119">Gibt die Quell Tresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="420ea-119">Specifies the source vault ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="420ea-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="420ea-120">-Confirm</span></span>
<span data-ttu-id="420ea-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="420ea-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="420ea-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="420ea-122">-WhatIf</span></span>
<span data-ttu-id="420ea-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="420ea-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="420ea-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="420ea-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="420ea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420ea-125">CommonParameters</span></span>
<span data-ttu-id="420ea-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="420ea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420ea-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="420ea-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420ea-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="420ea-128">INPUTS</span></span>

### <span data-ttu-id="420ea-129">Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="420ea-129">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="420ea-130">System. String</span><span class="sxs-lookup"><span data-stu-id="420ea-130">System.String</span></span>

## <span data-ttu-id="420ea-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="420ea-131">OUTPUTS</span></span>

### <span data-ttu-id="420ea-132">Microsoft. Azure. Management. Compute. Models. Disk</span><span class="sxs-lookup"><span data-stu-id="420ea-132">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="420ea-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="420ea-133">NOTES</span></span>

## <span data-ttu-id="420ea-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="420ea-134">RELATED LINKS</span></span>

