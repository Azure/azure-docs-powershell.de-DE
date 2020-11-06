---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubNamespace.md
ms.openlocfilehash: d65e19cb86a2ba850311fa937e64432ee8588d02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502581"
---
# <span data-ttu-id="c68e7-101">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="c68e7-101">Get-AzureRmEventHubNamespace</span></span>

## <span data-ttu-id="c68e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c68e7-102">SYNOPSIS</span></span>
<span data-ttu-id="c68e7-103">Ruft die Details eines Event Hubs-Namespaces ab oder ruft eine Liste aller Event Hubs-Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c68e7-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c68e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c68e7-104">SYNTAX</span></span>

```
Get-AzureRmEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c68e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c68e7-105">DESCRIPTION</span></span>
<span data-ttu-id="c68e7-106">Das Get-AzureRmEventHubNamespace-Cmdlet ruft entweder die Details eines angegebenen Event Hubs-Namespaces oder eine Liste aller Event Hubs-Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="c68e7-106">The Get-AzureRmEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="c68e7-107">Wenn der Namespacename angegeben wird, werden die Details eines einzelnen Event Hubs-Namespaces zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c68e7-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="c68e7-108">Wenn der Namespacename nicht angegeben wird, wird eine Liste mit Namespaces zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c68e7-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="c68e7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c68e7-109">EXAMPLES</span></span>

### <span data-ttu-id="c68e7-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c68e7-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="c68e7-111">Ruft die Details des Event Hubs-Namespace \` mynamespacename \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="c68e7-111">Gets the details of the Event Hubs namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c68e7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c68e7-112">PARAMETERS</span></span>

### <span data-ttu-id="c68e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c68e7-113">-DefaultProfile</span></span>
<span data-ttu-id="c68e7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c68e7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c68e7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c68e7-115">-Name</span></span>
<span data-ttu-id="c68e7-116">EventHub-Namespace Name</span><span class="sxs-lookup"><span data-stu-id="c68e7-116">EventHub Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c68e7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c68e7-117">-ResourceGroupName</span></span>
<span data-ttu-id="c68e7-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c68e7-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c68e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68e7-119">CommonParameters</span></span>
<span data-ttu-id="c68e7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c68e7-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68e7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68e7-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c68e7-122">INPUTS</span></span>

### <span data-ttu-id="c68e7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="c68e7-123">System.String</span></span>


## <span data-ttu-id="c68e7-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c68e7-124">OUTPUTS</span></span>

### <span data-ttu-id="c68e7-125">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c68e7-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="c68e7-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="c68e7-126">NOTES</span></span>

## <span data-ttu-id="c68e7-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c68e7-127">RELATED LINKS</span></span>
