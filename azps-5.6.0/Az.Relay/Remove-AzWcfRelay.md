---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: f99a3a999baad580e04c6872f047c02d4a99091f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943750"
---
# <span data-ttu-id="d041b-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="d041b-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="d041b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d041b-102">SYNOPSIS</span></span>
<span data-ttu-id="d041b-103">Entfernt wcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d041b-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="d041b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d041b-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d041b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d041b-105">DESCRIPTION</span></span>
<span data-ttu-id="d041b-106">Das **Cmdlet Remove-AzWcfRelay** entfernt wcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="d041b-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="d041b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d041b-107">EXAMPLES</span></span>

### <span data-ttu-id="d041b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d041b-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="d041b-109">Entfernt wcfRelay `TestWCFRelay1` aus dem `TestNameSpace-Relay1` -Namespace.</span><span class="sxs-lookup"><span data-stu-id="d041b-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="d041b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d041b-110">PARAMETERS</span></span>

### <span data-ttu-id="d041b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d041b-111">-DefaultProfile</span></span>
<span data-ttu-id="d041b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d041b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d041b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="d041b-113">-Name</span></span>
<span data-ttu-id="d041b-114">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="d041b-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="d041b-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d041b-115">-Namespace</span></span>
<span data-ttu-id="d041b-116">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="d041b-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d041b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d041b-117">-ResourceGroupName</span></span>
<span data-ttu-id="d041b-118">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d041b-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="d041b-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d041b-119">-Confirm</span></span>
<span data-ttu-id="d041b-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d041b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d041b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d041b-121">-WhatIf</span></span>
<span data-ttu-id="d041b-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d041b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d041b-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d041b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d041b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d041b-124">CommonParameters</span></span>
<span data-ttu-id="d041b-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d041b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d041b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d041b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d041b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d041b-127">INPUTS</span></span>

### <span data-ttu-id="d041b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d041b-128">System.String</span></span>

## <span data-ttu-id="d041b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d041b-129">OUTPUTS</span></span>

### <span data-ttu-id="d041b-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="d041b-130">System.Void</span></span>

## <span data-ttu-id="d041b-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d041b-131">NOTES</span></span>

## <span data-ttu-id="d041b-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d041b-132">RELATED LINKS</span></span>
