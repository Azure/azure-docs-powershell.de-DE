---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azdiskencryptionsetconfig.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSetConfig.md
ms.openlocfilehash: 358481a4c8ba20e8c8aa6f2ed47ebaa13225b939
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921416"
---
# <span data-ttu-id="be87e-101">New-AzDiskEncryptionSetConfig</span><span class="sxs-lookup"><span data-stu-id="be87e-101">New-AzDiskEncryptionSetConfig</span></span>

## <span data-ttu-id="be87e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be87e-102">SYNOPSIS</span></span>
<span data-ttu-id="be87e-103">Erstellt ein konfigurierbares Datenträgerverschlüsselungssatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="be87e-103">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="be87e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be87e-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSetConfig [-Location] <String> [[-Tag] <Hashtable>] [[-IdentityType] <String>]
 [[-SourceVaultId] <String>] [-KeyUrl <String>] [-EncryptionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be87e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="be87e-105">DESCRIPTION</span></span>
<span data-ttu-id="be87e-106">Erstellt ein konfigurierbares Datenträgerverschlüsselungssatzobjekt.</span><span class="sxs-lookup"><span data-stu-id="be87e-106">Creates a configurable disk encryption set object.</span></span>

## <span data-ttu-id="be87e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="be87e-107">EXAMPLES</span></span>

### <span data-ttu-id="be87e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="be87e-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="be87e-109">Erstellt einen Datenträgerverschlüsselungssatz mit dem angegebenen aktiven Schlüssel im Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="be87e-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="be87e-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="be87e-110">PARAMETERS</span></span>

### <span data-ttu-id="be87e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be87e-111">-DefaultProfile</span></span>
<span data-ttu-id="be87e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="be87e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be87e-113">-EncryptionType</span><span class="sxs-lookup"><span data-stu-id="be87e-113">-EncryptionType</span></span>
<span data-ttu-id="be87e-114">Verwenden Sie diese, um den Verschlüsselungstyp des Datenträgerverschlüsselungssatzs zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="be87e-114">Use this to set the encryption type of the disk encryption set.</span></span> <span data-ttu-id="be87e-115">Verfügbare Werte sind: "EncryptionAtRestWithPlatformKey", "EncryptionAtRestWithCustomerKey".</span><span class="sxs-lookup"><span data-stu-id="be87e-115">Available values are: 'EncryptionAtRestWithPlatformKey', 'EncryptionAtRestWithCustomerKey'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be87e-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="be87e-116">-IdentityType</span></span>
<span data-ttu-id="be87e-117">Der Typ der verwalteten Identität, der vom DiskEncryptionSet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be87e-117">The type of Managed Identity used by the DiskEncryptionSet.</span></span> <span data-ttu-id="be87e-118">Nur SystemAssigned wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="be87e-118">Only SystemAssigned is supported.</span></span>

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

### <span data-ttu-id="be87e-119">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="be87e-119">-KeyUrl</span></span>
<span data-ttu-id="be87e-120">URL, die auf den aktiven Schlüssel in KeyVault verweist</span><span class="sxs-lookup"><span data-stu-id="be87e-120">Url pointing to the active key in KeyVault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be87e-121">-Location</span><span class="sxs-lookup"><span data-stu-id="be87e-121">-Location</span></span>
<span data-ttu-id="be87e-122">Gibt einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="be87e-122">Specifies a location.</span></span>

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

### <span data-ttu-id="be87e-123">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="be87e-123">-SourceVaultId</span></span>
<span data-ttu-id="be87e-124">Ressourcen-ID des KeyVault, das den aktiven Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="be87e-124">Resource id of the KeyVault containing the active key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be87e-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="be87e-125">-Tag</span></span>
<span data-ttu-id="be87e-126">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="be87e-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="be87e-127">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="be87e-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be87e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="be87e-128">-Confirm</span></span>
<span data-ttu-id="be87e-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="be87e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be87e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be87e-130">-WhatIf</span></span>
<span data-ttu-id="be87e-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="be87e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be87e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="be87e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be87e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be87e-133">CommonParameters</span></span>
<span data-ttu-id="be87e-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be87e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be87e-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be87e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be87e-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="be87e-136">INPUTS</span></span>

### <span data-ttu-id="be87e-137">System.String</span><span class="sxs-lookup"><span data-stu-id="be87e-137">System.String</span></span>

### <span data-ttu-id="be87e-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="be87e-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="be87e-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="be87e-139">OUTPUTS</span></span>

### <span data-ttu-id="be87e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="be87e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="be87e-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="be87e-141">NOTES</span></span>

## <span data-ttu-id="be87e-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="be87e-142">RELATED LINKS</span></span>
