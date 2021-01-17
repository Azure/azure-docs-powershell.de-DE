---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 51a501e2b01ef044685f4172d42bad5342cb462c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472965"
---
# <span data-ttu-id="13b20-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="13b20-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="13b20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13b20-102">SYNOPSIS</span></span>
<span data-ttu-id="13b20-103">Legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Datenträgeraktualisierungsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="13b20-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="13b20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="13b20-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="13b20-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="13b20-105">DESCRIPTION</span></span>
<span data-ttu-id="13b20-106">Das **Cmdlet Set-AzDiskUpdateDiskEncryptionKey** legt die Eigenschaften des Datenträgerverschlüsselungsschlüssels für ein Datenträgeraktualisierungsobjekt fest.</span><span class="sxs-lookup"><span data-stu-id="13b20-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="13b20-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="13b20-107">EXAMPLES</span></span>

### <span data-ttu-id="13b20-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="13b20-108">Example 1</span></span>
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

<span data-ttu-id="13b20-109">Der erste Befehl erstellt ein lokales leeres Datenträgeraktualisierungsobjekt mit einer Größe von 10 GB im Premium_LRS Speicherkontotyp.</span><span class="sxs-lookup"><span data-stu-id="13b20-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="13b20-110">Außerdem wird der Typ des Windows-Betriebssystems festgelegt und Verschlüsselungseinstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="13b20-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="13b20-111">Mit dem zweiten und dritten Befehl werden der Datenträgerverschlüsselungsschlüssel und die Schlüsselverschlüsselungsschlüsseleinstellungen für das Datenträgeraktualisierungsobjekt festgelegt.</span><span class="sxs-lookup"><span data-stu-id="13b20-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="13b20-112">Der letzte Befehl übernimmt das Datenträgeraktualisierungsobjekt und aktualisiert einen vorhandenen Datenträger mit dem Namen 'Disk01' in der Ressourcengruppe 'ResourceGroup01'.</span><span class="sxs-lookup"><span data-stu-id="13b20-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="13b20-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13b20-113">PARAMETERS</span></span>

### <span data-ttu-id="13b20-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13b20-114">-DefaultProfile</span></span>
<span data-ttu-id="13b20-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="13b20-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13b20-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="13b20-116">-DiskUpdate</span></span>
<span data-ttu-id="13b20-117">Gibt ein Lokales Datenträgeraktualisierungsobjekt an.</span><span class="sxs-lookup"><span data-stu-id="13b20-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13b20-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="13b20-118">-SecretUrl</span></span>
<span data-ttu-id="13b20-119">Gibt die geheime URL an.</span><span class="sxs-lookup"><span data-stu-id="13b20-119">Specifies the secret Url.</span></span>

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

### <span data-ttu-id="13b20-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="13b20-120">-SourceVaultId</span></span>
<span data-ttu-id="13b20-121">Gibt die Quelltresor-ID an.</span><span class="sxs-lookup"><span data-stu-id="13b20-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="13b20-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="13b20-122">-Confirm</span></span>
<span data-ttu-id="13b20-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="13b20-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13b20-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="13b20-124">-WhatIf</span></span>
<span data-ttu-id="13b20-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="13b20-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="13b20-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="13b20-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13b20-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13b20-127">CommonParameters</span></span>
<span data-ttu-id="13b20-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13b20-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13b20-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13b20-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13b20-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="13b20-130">INPUTS</span></span>

### <span data-ttu-id="13b20-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="13b20-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="13b20-132">System.String</span><span class="sxs-lookup"><span data-stu-id="13b20-132">System.String</span></span>

## <span data-ttu-id="13b20-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="13b20-133">OUTPUTS</span></span>

### <span data-ttu-id="13b20-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="13b20-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="13b20-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="13b20-135">NOTES</span></span>

## <span data-ttu-id="13b20-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="13b20-136">RELATED LINKS</span></span>
