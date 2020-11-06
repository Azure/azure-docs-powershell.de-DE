---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: ab49458426b7035a20e63ca62d86124d79291b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496898"
---
# <span data-ttu-id="3226c-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="3226c-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="3226c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3226c-102">SYNOPSIS</span></span>
<span data-ttu-id="3226c-103">Ruft einen oder mehrere Server Verwaltungsknoten ab.</span><span class="sxs-lookup"><span data-stu-id="3226c-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3226c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3226c-104">SYNTAX</span></span>

### <span data-ttu-id="3226c-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="3226c-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3226c-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="3226c-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3226c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3226c-107">DESCRIPTION</span></span>
<span data-ttu-id="3226c-108">Das Cmdlet " **Get-AzureRmServerManagementNode** " Ruft einen oder mehrere Azure Server-Verwaltungsknoten ab.</span><span class="sxs-lookup"><span data-stu-id="3226c-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="3226c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3226c-109">EXAMPLES</span></span>

## <span data-ttu-id="3226c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3226c-110">PARAMETERS</span></span>

### <span data-ttu-id="3226c-111">-Node</span><span class="sxs-lookup"><span data-stu-id="3226c-111">-Node</span></span>
<span data-ttu-id="3226c-112">Gibt einen vorhandenen Knoten an, aus dem die *ResourceGroupName* und die *NodeName* -Parameter abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="3226c-112">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3226c-113">-Nodename</span><span class="sxs-lookup"><span data-stu-id="3226c-113">-NodeName</span></span>
<span data-ttu-id="3226c-114">Gibt den Namen des Knotens an, für den dieses Cmdlet abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3226c-114">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3226c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3226c-115">-ResourceGroupName</span></span>
<span data-ttu-id="3226c-116">Gibt den Namen der Ressourcengruppe an, zu der die Knoten gehören.</span><span class="sxs-lookup"><span data-stu-id="3226c-116">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3226c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3226c-117">-DefaultProfile</span></span>
<span data-ttu-id="3226c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3226c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3226c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3226c-119">CommonParameters</span></span>
<span data-ttu-id="3226c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3226c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3226c-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3226c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3226c-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3226c-122">INPUTS</span></span>

### <span data-ttu-id="3226c-123">Knoten</span><span class="sxs-lookup"><span data-stu-id="3226c-123">Node</span></span>
<span data-ttu-id="3226c-124">Der Parameter "Node" akzeptiert den Wert vom Typ "Node" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3226c-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="3226c-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3226c-125">OUTPUTS</span></span>

### <span data-ttu-id="3226c-126">Microsoft. Azure. Commands. Servermanagement. Modell. Node</span><span class="sxs-lookup"><span data-stu-id="3226c-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="3226c-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="3226c-127">NOTES</span></span>

## <span data-ttu-id="3226c-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3226c-128">RELATED LINKS</span></span>

[<span data-ttu-id="3226c-129">Neu – AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="3226c-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="3226c-130">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="3226c-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


