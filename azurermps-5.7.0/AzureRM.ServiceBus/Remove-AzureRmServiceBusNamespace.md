---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 5d58fe0b998f7998da7b3a456d005570929cb848
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663043"
---
# <span data-ttu-id="245b5-101">Remove-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="245b5-101">Remove-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="245b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="245b5-102">SYNOPSIS</span></span>
<span data-ttu-id="245b5-103">Entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="245b5-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="245b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="245b5-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="245b5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="245b5-105">DESCRIPTION</span></span>
<span data-ttu-id="245b5-106">Das Cmdlet **Remove-AzureRmServiceBusNamespace** entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="245b5-106">The **Remove-AzureRmServiceBusNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="245b5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="245b5-107">EXAMPLES</span></span>

### <span data-ttu-id="245b5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="245b5-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="245b5-109">Entfernt den ServiceBus-Namespace `SB-Example1` aus der angegebenen Ressourcengruppe `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="245b5-109">Removes the Service Bus namespace `SB-Example1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="245b5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="245b5-110">PARAMETERS</span></span>

### <span data-ttu-id="245b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245b5-111">-DefaultProfile</span></span>
<span data-ttu-id="245b5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="245b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="245b5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="245b5-113">-Name</span></span>
<span data-ttu-id="245b5-114">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="245b5-114">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245b5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="245b5-115">-ResourceGroupName</span></span>
<span data-ttu-id="245b5-116">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="245b5-116">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245b5-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="245b5-117">-Confirm</span></span>
<span data-ttu-id="245b5-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="245b5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="245b5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="245b5-119">-WhatIf</span></span>
<span data-ttu-id="245b5-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="245b5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="245b5-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="245b5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="245b5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245b5-122">CommonParameters</span></span>
<span data-ttu-id="245b5-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="245b5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245b5-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="245b5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245b5-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="245b5-125">INPUTS</span></span>

### <span data-ttu-id="245b5-126">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="245b5-126">-ResourceGroup</span></span>
 <span data-ttu-id="245b5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="245b5-127">System.String</span></span>

### <span data-ttu-id="245b5-128">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="245b5-128">-NamespaceName</span></span>
 <span data-ttu-id="245b5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="245b5-129">System.String</span></span>

## <span data-ttu-id="245b5-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="245b5-130">OUTPUTS</span></span>

### <span data-ttu-id="245b5-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="245b5-131">System.Object</span></span>

## <span data-ttu-id="245b5-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="245b5-132">NOTES</span></span>

## <span data-ttu-id="245b5-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="245b5-133">RELATED LINKS</span></span>

