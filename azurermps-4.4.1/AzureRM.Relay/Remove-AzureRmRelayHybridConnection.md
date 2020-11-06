---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 7f65f77d9d1f525dd8850c6934263b608d241751
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501642"
---
# <span data-ttu-id="7dcc1-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="7dcc1-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="7dcc1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7dcc1-102">SYNOPSIS</span></span>
<span data-ttu-id="7dcc1-103">Entfernt die HybridConnection aus dem angegebenen HybridConnection-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dcc1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7dcc1-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dcc1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7dcc1-105">DESCRIPTION</span></span>
<span data-ttu-id="7dcc1-106">Das Cmdlet **Remove-AzureRmRelayHybridConnection** entfernt die HybridConnection aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="7dcc1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7dcc1-107">EXAMPLES</span></span>

### <span data-ttu-id="7dcc1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7dcc1-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="7dcc1-109">Entfernt die HybridConnection `TestHybridConnection` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="7dcc1-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="7dcc1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7dcc1-110">PARAMETERS</span></span>

### <span data-ttu-id="7dcc1-111">-Name</span><span class="sxs-lookup"><span data-stu-id="7dcc1-111">-Name</span></span>
<span data-ttu-id="7dcc1-112">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-112">HybridConnections Name.</span></span>

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

### <span data-ttu-id="7dcc1-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7dcc1-113">-Namespace</span></span>
<span data-ttu-id="7dcc1-114">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-114">Namespace Name.</span></span>

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

### <span data-ttu-id="7dcc1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dcc1-115">-ResourceGroupName</span></span>
<span data-ttu-id="7dcc1-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="7dcc1-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7dcc1-117">-Confirm</span></span>
<span data-ttu-id="7dcc1-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dcc1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dcc1-119">-WhatIf</span></span>
<span data-ttu-id="7dcc1-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dcc1-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dcc1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dcc1-122">-DefaultProfile</span></span>
<span data-ttu-id="7dcc1-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dcc1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dcc1-124">CommonParameters</span></span>
<span data-ttu-id="7dcc1-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dcc1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dcc1-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dcc1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dcc1-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7dcc1-127">INPUTS</span></span>

### <span data-ttu-id="7dcc1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dcc1-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="7dcc1-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7dcc1-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="7dcc1-130">-Name</span><span class="sxs-lookup"><span data-stu-id="7dcc1-130">-Name</span></span>
    System.String

## <span data-ttu-id="7dcc1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7dcc1-131">OUTPUTS</span></span>

### <span data-ttu-id="7dcc1-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="7dcc1-132">System.Object</span></span>

## <span data-ttu-id="7dcc1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="7dcc1-133">NOTES</span></span>

## <span data-ttu-id="7dcc1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7dcc1-134">RELATED LINKS</span></span>

