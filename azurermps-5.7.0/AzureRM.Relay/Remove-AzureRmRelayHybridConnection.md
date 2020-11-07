---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 872683cbf4e26601ec16f05256f0011b0441127c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663445"
---
# <span data-ttu-id="99015-101">Remove-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="99015-101">Remove-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="99015-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99015-102">SYNOPSIS</span></span>
<span data-ttu-id="99015-103">Entfernt die HybridConnection aus dem angegebenen HybridConnection-Namespace.</span><span class="sxs-lookup"><span data-stu-id="99015-103">Removes the HybridConnection from the specified HybridConnection namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99015-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99015-104">SYNTAX</span></span>

```
Remove-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99015-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99015-105">DESCRIPTION</span></span>
<span data-ttu-id="99015-106">Das Cmdlet **Remove-AzureRmRelayHybridConnection** entfernt die HybridConnection aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="99015-106">The **Remove-AzureRmRelayHybridConnection** cmdlet removes the HybridConnection from the specified Relay namespace.</span></span>

## <span data-ttu-id="99015-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99015-107">EXAMPLES</span></span>

### <span data-ttu-id="99015-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="99015-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="99015-109">Entfernt die HybridConnection `TestHybridConnection` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="99015-109">Removes the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="99015-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="99015-110">PARAMETERS</span></span>

### <span data-ttu-id="99015-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99015-111">-DefaultProfile</span></span>
<span data-ttu-id="99015-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="99015-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99015-113">-Name</span><span class="sxs-lookup"><span data-stu-id="99015-113">-Name</span></span>
<span data-ttu-id="99015-114">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="99015-114">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99015-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="99015-115">-Namespace</span></span>
<span data-ttu-id="99015-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="99015-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99015-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99015-117">-ResourceGroupName</span></span>
<span data-ttu-id="99015-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="99015-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99015-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="99015-119">-Confirm</span></span>
<span data-ttu-id="99015-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99015-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99015-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99015-121">-WhatIf</span></span>
<span data-ttu-id="99015-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99015-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99015-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99015-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99015-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99015-124">CommonParameters</span></span>
<span data-ttu-id="99015-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99015-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99015-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99015-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99015-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99015-127">INPUTS</span></span>

### <span data-ttu-id="99015-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99015-128">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="99015-129">-Namespace</span><span class="sxs-lookup"><span data-stu-id="99015-129">-Namespace</span></span>
    System.String

### <span data-ttu-id="99015-130">-Name</span><span class="sxs-lookup"><span data-stu-id="99015-130">-Name</span></span>
    System.String

## <span data-ttu-id="99015-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99015-131">OUTPUTS</span></span>

### <span data-ttu-id="99015-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="99015-132">System.Object</span></span>

## <span data-ttu-id="99015-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="99015-133">NOTES</span></span>

## <span data-ttu-id="99015-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99015-134">RELATED LINKS</span></span>

