---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskdiskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskDiskEncryptionKey.md
ms.openlocfilehash: 8ef1bccc711b96eb4b06c0b1234a426f9752208d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171149"
---
# <span data-ttu-id="62995-101">Set-AzDiskDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="62995-101">Set-AzDiskDiskEncryptionKey</span></span>

## <span data-ttu-id="62995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62995-102">SYNOPSIS</span></span>
<span data-ttu-id="62995-103">Legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="62995-103">Sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="62995-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62995-104">SYNTAX</span></span>

```
Set-AzDiskDiskEncryptionKey [-Disk] <PSDisk> [[-SecretUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62995-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62995-105">DESCRIPTION</span></span>
<span data-ttu-id="62995-106">Das **Cmdlet Set-AzDiskDiskEncryptionKey** legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Datenträgerobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="62995-106">The **Set-AzDiskDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk object.</span></span>

## <span data-ttu-id="62995-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62995-107">EXAMPLES</span></span>

### <span data-ttu-id="62995-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="62995-108">Example 1</span></span>
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

<span data-ttu-id="62995-109">Der erste Befehl erstellt ein lokales leeres Datenträgerobjekt mit einer Größe von 5 GB im Standard_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="62995-109">The first command creates a local empty disk object with size 5GB in Standard_LRS storage account type.</span></span>  <span data-ttu-id="62995-110">Außerdem wird der Typ des Windows-Betriebssystems festgelegt, und es werden Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="62995-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="62995-111">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Datenträgerobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="62995-111">The second and third commands set the disk encryption key and key encryption key settings for the disk object.</span></span>
<span data-ttu-id="62995-112">Der letzte Befehl übernimmt das Datenträgerobjekt und erstellt einen Datenträger mit dem Namen 'Disk01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="62995-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="62995-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62995-113">PARAMETERS</span></span>

### <span data-ttu-id="62995-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62995-114">-DefaultProfile</span></span>
<span data-ttu-id="62995-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62995-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62995-116">-Disk</span><span class="sxs-lookup"><span data-stu-id="62995-116">-Disk</span></span>
<span data-ttu-id="62995-117">Gibt ein lokales Datenträgerobjekt an.</span><span class="sxs-lookup"><span data-stu-id="62995-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="62995-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="62995-118">-SecretUrl</span></span>
<span data-ttu-id="62995-119">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="62995-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="62995-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="62995-120">-SourceVaultId</span></span>
<span data-ttu-id="62995-121">Gibt die Quelltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="62995-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="62995-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62995-122">-Confirm</span></span>
<span data-ttu-id="62995-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62995-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62995-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="62995-124">-WhatIf</span></span>
<span data-ttu-id="62995-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62995-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62995-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62995-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62995-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62995-127">CommonParameters</span></span>
<span data-ttu-id="62995-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62995-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62995-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62995-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62995-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62995-130">INPUTS</span></span>

### <span data-ttu-id="62995-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="62995-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="62995-132">System.String</span><span class="sxs-lookup"><span data-stu-id="62995-132">System.String</span></span>

## <span data-ttu-id="62995-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62995-133">OUTPUTS</span></span>

### <span data-ttu-id="62995-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="62995-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="62995-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="62995-135">NOTES</span></span>

## <span data-ttu-id="62995-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="62995-136">RELATED LINKS</span></span>
