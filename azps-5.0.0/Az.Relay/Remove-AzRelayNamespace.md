---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayNamespace.md
ms.openlocfilehash: 463ef6d1d23ffe809d8810a9cbf4dd0ebf1ff578
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302560"
---
# <span data-ttu-id="8c7a1-101">Remove-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="8c7a1-101">Remove-AzRelayNamespace</span></span>

## <span data-ttu-id="8c7a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c7a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7a1-103">Entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-103">Removes the namespace from the specified resource group.</span></span> 

## <span data-ttu-id="8c7a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c7a1-104">SYNTAX</span></span>

```
Remove-AzRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c7a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c7a1-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7a1-106">Das Cmdlet **Remove-AzRelayNamespace** entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-106">The **Remove-AzRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="8c7a1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c7a1-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7a1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8c7a1-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="8c7a1-109">Entfernt den Relay `TestNameSpace-Relay1` -Namespace aus der angegebenen Ressourcengruppe `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="8c7a1-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="8c7a1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c7a1-110">PARAMETERS</span></span>

### <span data-ttu-id="8c7a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7a1-111">-DefaultProfile</span></span>
<span data-ttu-id="8c7a1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c7a1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8c7a1-113">-Name</span></span>
<span data-ttu-id="8c7a1-114">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="8c7a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="8c7a1-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c7a1-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c7a1-117">-Confirm</span></span>
<span data-ttu-id="8c7a1-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c7a1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c7a1-119">-WhatIf</span></span>
<span data-ttu-id="8c7a1-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c7a1-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c7a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7a1-122">CommonParameters</span></span>
<span data-ttu-id="8c7a1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c7a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7a1-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c7a1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7a1-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c7a1-125">INPUTS</span></span>

### <span data-ttu-id="8c7a1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8c7a1-126">System.String</span></span>

## <span data-ttu-id="8c7a1-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c7a1-127">OUTPUTS</span></span>

### <span data-ttu-id="8c7a1-128">System. void</span><span class="sxs-lookup"><span data-stu-id="8c7a1-128">System.Void</span></span>

## <span data-ttu-id="8c7a1-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c7a1-129">NOTES</span></span>

## <span data-ttu-id="8c7a1-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c7a1-130">RELATED LINKS</span></span>
