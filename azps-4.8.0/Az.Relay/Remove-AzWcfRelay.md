---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzWcfRelay.md
ms.openlocfilehash: 238c4ecf92cbdd1dc6e9e0a430ec8e6ad200b967
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008982"
---
# <span data-ttu-id="a40ae-101">Remove-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="a40ae-101">Remove-AzWcfRelay</span></span>

## <span data-ttu-id="a40ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a40ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a40ae-103">Entfernt die WcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a40ae-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="a40ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a40ae-104">SYNTAX</span></span>

```
Remove-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a40ae-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a40ae-105">DESCRIPTION</span></span>
<span data-ttu-id="a40ae-106">Das Cmdlet **Remove-AzWcfRelay** entfernt die WcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a40ae-106">The **Remove-AzWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="a40ae-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a40ae-107">EXAMPLES</span></span>

### <span data-ttu-id="a40ae-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a40ae-108">Example 1</span></span>
```
PS C:\> Remove-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="a40ae-109">Entfernt die WcfRelay `TestWCFRelay1` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="a40ae-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="a40ae-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a40ae-110">PARAMETERS</span></span>

### <span data-ttu-id="a40ae-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a40ae-111">-DefaultProfile</span></span>
<span data-ttu-id="a40ae-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a40ae-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a40ae-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a40ae-113">-Name</span></span>
<span data-ttu-id="a40ae-114">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="a40ae-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="a40ae-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a40ae-115">-Namespace</span></span>
<span data-ttu-id="a40ae-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="a40ae-116">Namespace Name.</span></span>

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

### <span data-ttu-id="a40ae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a40ae-117">-ResourceGroupName</span></span>
<span data-ttu-id="a40ae-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a40ae-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="a40ae-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a40ae-119">-Confirm</span></span>
<span data-ttu-id="a40ae-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a40ae-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a40ae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a40ae-121">-WhatIf</span></span>
<span data-ttu-id="a40ae-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a40ae-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a40ae-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a40ae-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a40ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40ae-124">CommonParameters</span></span>
<span data-ttu-id="a40ae-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40ae-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40ae-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40ae-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a40ae-127">INPUTS</span></span>

### <span data-ttu-id="a40ae-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a40ae-128">System.String</span></span>

## <span data-ttu-id="a40ae-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a40ae-129">OUTPUTS</span></span>

### <span data-ttu-id="a40ae-130">System. void</span><span class="sxs-lookup"><span data-stu-id="a40ae-130">System.Void</span></span>

## <span data-ttu-id="a40ae-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a40ae-131">NOTES</span></span>

## <span data-ttu-id="a40ae-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a40ae-132">RELATED LINKS</span></span>
