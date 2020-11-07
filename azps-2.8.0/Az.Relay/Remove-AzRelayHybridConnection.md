---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/remove-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Remove-AzRelayHybridConnection.md
ms.openlocfilehash: b0d7ef4a3fcaf681ea52719a5c7627784dac8d65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823583"
---
# <span data-ttu-id="b0e28-101">Remove-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="b0e28-101">Remove-AzRelayHybridConnection</span></span>

## <span data-ttu-id="b0e28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0e28-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e28-103">Entfernt die HybridConnection aus dem angegebenen HybridConnection-Namespace.</span><span class="sxs-lookup"><span data-stu-id="b0e28-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

## <span data-ttu-id="b0e28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0e28-104">SYNTAX</span></span>

```
Remove-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0e28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0e28-105">DESCRIPTION</span></span>
<span data-ttu-id="b0e28-106">Das Cmdlet **Remove-AzRelayHybridConnection** entfernt die HybridConnection aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="b0e28-106">The **Remove-AzRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="b0e28-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0e28-107">EXAMPLES</span></span>

### <span data-ttu-id="b0e28-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b0e28-108">Example 1</span></span>
```
PS C:\> Remove-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="b0e28-109">Entfernt die HybridConnection `TestHybridConnection` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="b0e28-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="b0e28-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0e28-110">PARAMETERS</span></span>

### <span data-ttu-id="b0e28-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e28-111">-DefaultProfile</span></span>
<span data-ttu-id="b0e28-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0e28-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0e28-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b0e28-113">-Name</span></span>
<span data-ttu-id="b0e28-114">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="b0e28-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="b0e28-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b0e28-115">-Namespace</span></span>
<span data-ttu-id="b0e28-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="b0e28-116">Namespace Name.</span></span>

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

### <span data-ttu-id="b0e28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e28-117">-ResourceGroupName</span></span>
<span data-ttu-id="b0e28-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b0e28-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0e28-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b0e28-119">-Confirm</span></span>
<span data-ttu-id="b0e28-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0e28-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0e28-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0e28-121">-WhatIf</span></span>
<span data-ttu-id="b0e28-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0e28-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0e28-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0e28-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0e28-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e28-124">CommonParameters</span></span>
<span data-ttu-id="b0e28-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e28-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e28-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e28-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e28-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0e28-127">INPUTS</span></span>

### <span data-ttu-id="b0e28-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b0e28-128">System.String</span></span>

## <span data-ttu-id="b0e28-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0e28-129">OUTPUTS</span></span>

### <span data-ttu-id="b0e28-130">System. void</span><span class="sxs-lookup"><span data-stu-id="b0e28-130">System.Void</span></span>

## <span data-ttu-id="b0e28-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0e28-131">NOTES</span></span>

## <span data-ttu-id="b0e28-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0e28-132">RELATED LINKS</span></span>
