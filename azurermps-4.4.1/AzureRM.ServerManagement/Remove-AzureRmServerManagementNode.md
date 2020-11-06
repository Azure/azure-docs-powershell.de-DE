---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 93efff5a9f317b7d44d071a4dd212d235df02223
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496866"
---
# <span data-ttu-id="5c6c4-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="5c6c4-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="5c6c4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c6c4-102">SYNOPSIS</span></span>
<span data-ttu-id="5c6c4-103">Entfernt einen Server Verwaltungsknoten.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c6c4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c6c4-104">SYNTAX</span></span>

### <span data-ttu-id="5c6c4-105">ByName</span><span class="sxs-lookup"><span data-stu-id="5c6c4-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c6c4-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="5c6c4-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c6c4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c6c4-107">DESCRIPTION</span></span>
<span data-ttu-id="5c6c4-108">Das Cmdlet **Remove-AzureRmServerManagementNode** entfernt einen Azure Server Management-Knoten.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="5c6c4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c6c4-109">EXAMPLES</span></span>

## <span data-ttu-id="5c6c4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c6c4-110">PARAMETERS</span></span>

### <span data-ttu-id="5c6c4-111">-Node</span><span class="sxs-lookup"><span data-stu-id="5c6c4-111">-Node</span></span>
<span data-ttu-id="5c6c4-112">Gibt den Knoten an, für den dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-112">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="5c6c4-113">Dieser Parameter kann anstelle der *ResourceGroupName* -und *NodeName* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-113">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c6c4-114">-Nodename</span><span class="sxs-lookup"><span data-stu-id="5c6c4-114">-NodeName</span></span>
<span data-ttu-id="5c6c4-115">Gibt den Namen des Knotens an, für den dieses Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-115">Specifies the name of the node for which this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c6c4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c6c4-116">-ResourceGroupName</span></span>
<span data-ttu-id="5c6c4-117">Gibt den Namen der Ressourcengruppe an, zu der der Knoten gehört.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-117">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c6c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c6c4-118">-DefaultProfile</span></span>
<span data-ttu-id="5c6c4-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c6c4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c6c4-120">CommonParameters</span></span>
<span data-ttu-id="5c6c4-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c6c4-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c6c4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c6c4-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c6c4-123">INPUTS</span></span>

### <span data-ttu-id="5c6c4-124">Knoten</span><span class="sxs-lookup"><span data-stu-id="5c6c4-124">Node</span></span>
<span data-ttu-id="5c6c4-125">Der Parameter "Node" akzeptiert den Wert vom Typ "Node" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5c6c4-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="5c6c4-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c6c4-126">OUTPUTS</span></span>

## <span data-ttu-id="5c6c4-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c6c4-127">NOTES</span></span>

## <span data-ttu-id="5c6c4-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c6c4-128">RELATED LINKS</span></span>

[<span data-ttu-id="5c6c4-129">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="5c6c4-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="5c6c4-130">Neu – AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="5c6c4-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


