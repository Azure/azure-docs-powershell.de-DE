---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e3388a06a2835fcd9865a9aa46d376b693152bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496894"
---
# <span data-ttu-id="6ee79-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="6ee79-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="6ee79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ee79-102">SYNOPSIS</span></span>
<span data-ttu-id="6ee79-103">Ruft eine Server Verwaltungssitzung ab.</span><span class="sxs-lookup"><span data-stu-id="6ee79-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ee79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ee79-104">SYNTAX</span></span>

### <span data-ttu-id="6ee79-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="6ee79-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ee79-106">BySession</span><span class="sxs-lookup"><span data-stu-id="6ee79-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ee79-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="6ee79-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ee79-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ee79-108">DESCRIPTION</span></span>
<span data-ttu-id="6ee79-109">Das Cmdlet " **Get-AzureRmServerManagementSession** " Ruft eine einzelne Azure Server-Verwaltungssitzung ab.</span><span class="sxs-lookup"><span data-stu-id="6ee79-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="6ee79-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ee79-110">EXAMPLES</span></span>

## <span data-ttu-id="6ee79-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ee79-111">PARAMETERS</span></span>

### <span data-ttu-id="6ee79-112">-Node</span><span class="sxs-lookup"><span data-stu-id="6ee79-112">-Node</span></span>
<span data-ttu-id="6ee79-113">Gibt ein vorhandenes **Node** -Objekt an, das zum Abrufen der *ResourceGroupName* -und *NodeName* -Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ee79-113">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="6ee79-114">Außerdem müssen Sie einen Wert für den *Sessionname* -Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="6ee79-114">You must also specify a value for the *SessionName* parameter.</span></span>

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

### <span data-ttu-id="6ee79-115">-Nodename</span><span class="sxs-lookup"><span data-stu-id="6ee79-115">-NodeName</span></span>
<span data-ttu-id="6ee79-116">Gibt den Namen des Knotens an, in dem sich die Sitzung befindet.</span><span class="sxs-lookup"><span data-stu-id="6ee79-116">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ee79-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ee79-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet das Abrufen der Sitzung abruft.</span><span class="sxs-lookup"><span data-stu-id="6ee79-118">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee79-119">-Sitzung</span><span class="sxs-lookup"><span data-stu-id="6ee79-119">-Session</span></span>
<span data-ttu-id="6ee79-120">Gibt ein vorhandenes **Session** -Objekt an, das zum Abrufen der *ResourceGroupName* , des *NodeName* und des *Sessionname* -Parameters verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6ee79-120">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ee79-121">-Sitzungsname</span><span class="sxs-lookup"><span data-stu-id="6ee79-121">-SessionName</span></span>
<span data-ttu-id="6ee79-122">Gibt den Namen der Sitzung an, in der das Cmdlet abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6ee79-122">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ee79-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ee79-123">-DefaultProfile</span></span>
<span data-ttu-id="6ee79-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6ee79-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ee79-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ee79-125">CommonParameters</span></span>
<span data-ttu-id="6ee79-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ee79-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ee79-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ee79-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ee79-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ee79-128">INPUTS</span></span>

### <span data-ttu-id="6ee79-129">Knoten</span><span class="sxs-lookup"><span data-stu-id="6ee79-129">Node</span></span>
<span data-ttu-id="6ee79-130">Der Parameter "Node" akzeptiert den Wert vom Typ "Node" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6ee79-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="6ee79-131">Sitzung</span><span class="sxs-lookup"><span data-stu-id="6ee79-131">Session</span></span>
<span data-ttu-id="6ee79-132">Der Parameter "Session" akzeptiert den Wert vom Typ "Session" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6ee79-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="6ee79-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ee79-133">OUTPUTS</span></span>

### <span data-ttu-id="6ee79-134">Microsoft. Azure. Commands. Servermanagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="6ee79-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="6ee79-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ee79-135">NOTES</span></span>

## <span data-ttu-id="6ee79-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ee79-136">RELATED LINKS</span></span>

[<span data-ttu-id="6ee79-137">Azure Server-Verwaltungs-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6ee79-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


