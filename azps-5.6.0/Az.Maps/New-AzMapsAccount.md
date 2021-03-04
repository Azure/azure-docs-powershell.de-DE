---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: b6a2e27f18a0ae9b7c98239d5acd1073922e149e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946085"
---
# <span data-ttu-id="b4db4-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b4db4-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="b4db4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4db4-102">SYNOPSIS</span></span>
<span data-ttu-id="b4db4-103">Erstellt ein Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="b4db4-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="b4db4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b4db4-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4db4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4db4-105">DESCRIPTION</span></span>
<span data-ttu-id="b4db4-106">Das New-AzMapsAccount-Cmdlet erstellt ein Azure Maps-Konto mit der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="b4db4-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="b4db4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b4db4-107">EXAMPLES</span></span>

### <span data-ttu-id="b4db4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4db4-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="b4db4-109">Erstellt ein neues Azure Maps-Konto mit dem Namen MyAccount in der Ressourcengruppe MyResourceGroup mit der SKU S0 und einem Tag.</span><span class="sxs-lookup"><span data-stu-id="b4db4-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="b4db4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b4db4-110">PARAMETERS</span></span>

### <span data-ttu-id="b4db4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4db4-111">-DefaultProfile</span></span>
<span data-ttu-id="b4db4-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b4db4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4db4-113">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="b4db4-113">-Force</span></span>
<span data-ttu-id="b4db4-114">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="b4db4-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="b4db4-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b4db4-115">-Name</span></span>
<span data-ttu-id="b4db4-116">Karten-Kontoname.</span><span class="sxs-lookup"><span data-stu-id="b4db4-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4db4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4db4-117">-ResourceGroupName</span></span>
<span data-ttu-id="b4db4-118">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b4db4-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="b4db4-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b4db4-119">-SkuName</span></span>
<span data-ttu-id="b4db4-120">Karten Konto-Sku-Name.</span><span class="sxs-lookup"><span data-stu-id="b4db4-120">Maps Account Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4db4-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4db4-121">-Tag</span></span>
<span data-ttu-id="b4db4-122">Karten-Kontotags.</span><span class="sxs-lookup"><span data-stu-id="b4db4-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4db4-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4db4-123">-Confirm</span></span>
<span data-ttu-id="b4db4-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4db4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4db4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4db4-125">-WhatIf</span></span>
<span data-ttu-id="b4db4-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4db4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4db4-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4db4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4db4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4db4-128">CommonParameters</span></span>
<span data-ttu-id="b4db4-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4db4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4db4-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4db4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4db4-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b4db4-131">INPUTS</span></span>

### <span data-ttu-id="b4db4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b4db4-132">System.String</span></span>

## <span data-ttu-id="b4db4-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b4db4-133">OUTPUTS</span></span>

### <span data-ttu-id="b4db4-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="b4db4-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="b4db4-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b4db4-135">NOTES</span></span>

## <span data-ttu-id="b4db4-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b4db4-136">RELATED LINKS</span></span>
