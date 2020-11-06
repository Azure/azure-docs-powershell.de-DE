---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: 52abd413f94d0c190a6f03b3707efdb544a4b72a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480997"
---
# <span data-ttu-id="2790c-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="2790c-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="2790c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2790c-102">SYNOPSIS</span></span>
<span data-ttu-id="2790c-103">Entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2790c-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2790c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2790c-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2790c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2790c-105">DESCRIPTION</span></span>
<span data-ttu-id="2790c-106">Das Cmdlet **Remove-AzureRmRelayNamespace** entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2790c-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="2790c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2790c-107">EXAMPLES</span></span>

### <span data-ttu-id="2790c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2790c-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="2790c-109">Entfernt den Relay `TestNameSpace-Relay1` -Namespace aus der angegebenen Ressourcengruppe `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="2790c-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="2790c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2790c-110">PARAMETERS</span></span>

### <span data-ttu-id="2790c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2790c-111">-DefaultProfile</span></span>
<span data-ttu-id="2790c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2790c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2790c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2790c-113">-Name</span></span>
<span data-ttu-id="2790c-114">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="2790c-114">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="2790c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2790c-115">-ResourceGroupName</span></span>
<span data-ttu-id="2790c-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2790c-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="2790c-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2790c-117">-Confirm</span></span>
<span data-ttu-id="2790c-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2790c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2790c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2790c-119">-WhatIf</span></span>
<span data-ttu-id="2790c-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2790c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2790c-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2790c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2790c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2790c-122">CommonParameters</span></span>
<span data-ttu-id="2790c-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2790c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2790c-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2790c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2790c-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2790c-125">INPUTS</span></span>

### <span data-ttu-id="2790c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2790c-126">-ResourceGroupName</span></span>
 <span data-ttu-id="2790c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2790c-127">System.String</span></span>

### <span data-ttu-id="2790c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2790c-128">-Name</span></span>
 <span data-ttu-id="2790c-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2790c-129">System.String</span></span>

## <span data-ttu-id="2790c-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2790c-130">OUTPUTS</span></span>

### <span data-ttu-id="2790c-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="2790c-131">System.Object</span></span>

## <span data-ttu-id="2790c-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="2790c-132">NOTES</span></span>

## <span data-ttu-id="2790c-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2790c-133">RELATED LINKS</span></span>

