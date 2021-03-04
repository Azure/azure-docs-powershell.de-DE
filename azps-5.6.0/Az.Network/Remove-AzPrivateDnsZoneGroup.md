---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: ada7faf13457f2c074a15b6e409e31afb93ac900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940043"
---
# <span data-ttu-id="87c98-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="87c98-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="87c98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87c98-102">SYNOPSIS</span></span>
<span data-ttu-id="87c98-103">Entfernt eine DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="87c98-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="87c98-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87c98-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87c98-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="87c98-105">DESCRIPTION</span></span>
<span data-ttu-id="87c98-106">Das **Cmdlet Remove-AzPrivateDnsZoneGroup** entfernt eine DNS-Zonengruppe.</span><span class="sxs-lookup"><span data-stu-id="87c98-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="87c98-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="87c98-107">EXAMPLES</span></span>

### <span data-ttu-id="87c98-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87c98-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="87c98-109">Im vorstehenden Beispiel wird ein DNS-Zonen-Grup mit dem Namen dnsgroup1 aus endpunkttest-pr-endpoint entfernt.</span><span class="sxs-lookup"><span data-stu-id="87c98-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="87c98-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="87c98-110">PARAMETERS</span></span>

### <span data-ttu-id="87c98-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87c98-111">-AsJob</span></span>
<span data-ttu-id="87c98-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="87c98-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87c98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87c98-113">-DefaultProfile</span></span>
<span data-ttu-id="87c98-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87c98-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87c98-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="87c98-115">-Force</span></span>
<span data-ttu-id="87c98-116">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="87c98-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="87c98-117">-Name</span><span class="sxs-lookup"><span data-stu-id="87c98-117">-Name</span></span>
<span data-ttu-id="87c98-118">Der Name der gruppe für private DNS-Zonen.</span><span class="sxs-lookup"><span data-stu-id="87c98-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c98-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87c98-119">-PassThru</span></span>
<span data-ttu-id="87c98-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="87c98-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="87c98-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="87c98-121">-PrivateEndpointName</span></span>
<span data-ttu-id="87c98-122">Der Name des privaten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="87c98-122">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c98-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87c98-123">-ResourceGroupName</span></span>
<span data-ttu-id="87c98-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="87c98-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87c98-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87c98-125">-Confirm</span></span>
<span data-ttu-id="87c98-126">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87c98-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87c98-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87c98-127">-WhatIf</span></span>
<span data-ttu-id="87c98-128">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87c98-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87c98-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87c98-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87c98-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87c98-130">CommonParameters</span></span>
<span data-ttu-id="87c98-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87c98-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87c98-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87c98-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87c98-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="87c98-133">INPUTS</span></span>

### <span data-ttu-id="87c98-134">System.String</span><span class="sxs-lookup"><span data-stu-id="87c98-134">System.String</span></span>

## <span data-ttu-id="87c98-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="87c98-135">OUTPUTS</span></span>

### <span data-ttu-id="87c98-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="87c98-136">System.Boolean</span></span>

## <span data-ttu-id="87c98-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="87c98-137">NOTES</span></span>

## <span data-ttu-id="87c98-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="87c98-138">RELATED LINKS</span></span>
