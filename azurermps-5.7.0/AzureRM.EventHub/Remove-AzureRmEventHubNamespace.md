---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubNamespace.md
ms.openlocfilehash: cec41bda56da33f22def6c44752effb3d705b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662852"
---
# <span data-ttu-id="40efb-101">Remove-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="40efb-101">Remove-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="40efb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40efb-102">SYNOPSIS</span></span>
<span data-ttu-id="40efb-103">Entfernt den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="40efb-103">Removes the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40efb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40efb-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40efb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40efb-105">DESCRIPTION</span></span>
<span data-ttu-id="40efb-106">Das Remove-AzureRmEventHubNamespace-Cmdlet entfernt den angegebenen Event Hubs-Namespace und löscht ihn.</span><span class="sxs-lookup"><span data-stu-id="40efb-106">The Remove-AzureRmEventHubNamespace cmdlet removes and deletes the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="40efb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40efb-107">EXAMPLES</span></span>

### <span data-ttu-id="40efb-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40efb-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName
```

<span data-ttu-id="40efb-109">Entfernt den Event Hubs \` -Namespace mynamespacename \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="40efb-109">Removes the Event Hubs namespace \`MyNamespaceName\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="40efb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="40efb-110">PARAMETERS</span></span>

### <span data-ttu-id="40efb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40efb-111">-DefaultProfile</span></span>
<span data-ttu-id="40efb-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="40efb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40efb-113">-Name</span><span class="sxs-lookup"><span data-stu-id="40efb-113">-Name</span></span>
<span data-ttu-id="40efb-114">EventHub-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="40efb-114">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="40efb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40efb-115">-ResourceGroupName</span></span>
<span data-ttu-id="40efb-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="40efb-116">Resource Group Name</span></span>

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

### <span data-ttu-id="40efb-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="40efb-117">-Confirm</span></span>
<span data-ttu-id="40efb-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="40efb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40efb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40efb-119">-WhatIf</span></span>
<span data-ttu-id="40efb-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40efb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40efb-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="40efb-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40efb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40efb-122">CommonParameters</span></span>
<span data-ttu-id="40efb-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40efb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="40efb-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40efb-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40efb-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40efb-125">INPUTS</span></span>

### <span data-ttu-id="40efb-126">System. String</span><span class="sxs-lookup"><span data-stu-id="40efb-126">System.String</span></span>


## <span data-ttu-id="40efb-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40efb-127">OUTPUTS</span></span>

### <span data-ttu-id="40efb-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="40efb-128">System.Object</span></span>

## <span data-ttu-id="40efb-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="40efb-129">NOTES</span></span>

## <span data-ttu-id="40efb-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40efb-130">RELATED LINKS</span></span>
