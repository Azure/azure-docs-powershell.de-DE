---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: fbd10d4951a7b0bfccda304ec924894692b458ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930347"
---
# <span data-ttu-id="e076b-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e076b-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="e076b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e076b-102">SYNOPSIS</span></span>
<span data-ttu-id="e076b-103">Legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="e076b-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="e076b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e076b-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e076b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e076b-105">DESCRIPTION</span></span>
<span data-ttu-id="e076b-106">Das **Cmdlet Set-AzDiskDiskEncryptionKey** legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="e076b-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="e076b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e076b-107">EXAMPLES</span></span>

### <span data-ttu-id="e076b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e076b-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 5 -SkuName StandardLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskconfig = Set-AzDiskDiskEncryptionKey -Disk $diskconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskconfig = Set-AzDiskKeyEncryptionKey -Disk $diskconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> $diskConfig.EncryptionSettingsCollection.EncryptionSettingsVersion = '1.1'; 
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e076b-109">Mit dem ersten Befehl wird ein lokales leeres Datenträgerobjekt mit der Größe 5 GB im Standard_LRS Speicherkontotyp erstellt.</span><span class="sxs-lookup"><span data-stu-id="e076b-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="e076b-110">Außerdem wird der Windows -Betriebssystemtyp festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e076b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="e076b-111">Mit dem zweiten und dritten Befehl werden die Einstellungen für den Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüssel für das Datenträgerobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e076b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="e076b-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen "Disk01" in der Ressourcengruppe "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e076b-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e076b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e076b-113">PARAMETERS</span></span>

### <span data-ttu-id="e076b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e076b-114">-DefaultProfile</span></span>
<span data-ttu-id="e076b-115">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e076b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e076b-116">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="e076b-116">-Disk</span></span>
<span data-ttu-id="e076b-117">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="e076b-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e076b-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="e076b-118">-SecretUrl</span></span>
<span data-ttu-id="e076b-119">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="e076b-119">Specifies the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e076b-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="e076b-120">-SourceVaultId</span></span>
<span data-ttu-id="e076b-121">Gibt die Quelltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="e076b-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e076b-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e076b-122">-Confirm</span></span>
<span data-ttu-id="e076b-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e076b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e076b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e076b-124">-WhatIf</span></span>
<span data-ttu-id="e076b-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e076b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e076b-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e076b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e076b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e076b-127">CommonParameters</span></span>
<span data-ttu-id="e076b-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e076b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e076b-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e076b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e076b-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e076b-130">INPUTS</span></span>

### <span data-ttu-id="e076b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="e076b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="e076b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e076b-132">System.String</span></span>

## <span data-ttu-id="e076b-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e076b-133">OUTPUTS</span></span>

### <span data-ttu-id="e076b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="e076b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e076b-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e076b-135">NOTES</span></span>

## <span data-ttu-id="e076b-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e076b-136">RELATED LINKS</span></span>
