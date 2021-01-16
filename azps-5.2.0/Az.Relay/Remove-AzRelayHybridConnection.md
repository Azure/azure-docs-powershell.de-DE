---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: da563f063fb22ffd5c21dfc3d330a59a122c9a84
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357186"
---
# <span data-ttu-id="0406e-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="0406e-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="0406e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0406e-102">SYNOPSIS</span></span>
<span data-ttu-id="0406e-103">Entfernt die HybridVerbindung aus dem angegebenen HybridConnection-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0406e-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="0406e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0406e-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0406e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0406e-105">DESCRIPTION</span></span>
<span data-ttu-id="0406e-106">Das **Cmdlet "Remove-AzRelayHybridConnection"** entfernt die HybridVerbindung aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0406e-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="0406e-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0406e-107">EXAMPLES</span></span>

### <span data-ttu-id="0406e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0406e-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="0406e-109">Entfernt hybridconnection `TestHybridConnection` aus dem `TestNameSpace-Relay1` Namespace.</span><span class="sxs-lookup"><span data-stu-id="0406e-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="0406e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0406e-110">PARAMETERS</span></span>

### <span data-ttu-id="0406e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0406e-111">-DefaultProfile</span></span>
<span data-ttu-id="0406e-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0406e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0406e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0406e-113">-Name</span></span>
<span data-ttu-id="0406e-114">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="0406e-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="0406e-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0406e-115">-Namespace</span></span>
<span data-ttu-id="0406e-116">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="0406e-116">Namespace Name.</span></span>

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

### <span data-ttu-id="0406e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0406e-117">-ResourceGroupName</span></span>
<span data-ttu-id="0406e-118">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0406e-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="0406e-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0406e-119">-Confirm</span></span>
<span data-ttu-id="0406e-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0406e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0406e-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0406e-121">-WhatIf</span></span>
<span data-ttu-id="0406e-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0406e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0406e-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0406e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0406e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0406e-124">CommonParameters</span></span>
<span data-ttu-id="0406e-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0406e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0406e-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0406e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0406e-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0406e-127">INPUTS</span></span>

### <span data-ttu-id="0406e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0406e-128">System.String</span></span>

## <span data-ttu-id="0406e-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0406e-129">OUTPUTS</span></span>

### <span data-ttu-id="0406e-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="0406e-130">System.Void</span></span>

## <span data-ttu-id="0406e-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0406e-131">NOTES</span></span>

## <span data-ttu-id="0406e-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0406e-132">RELATED LINKS</span></span>
