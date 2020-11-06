---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 7d8b2e02e5683f58eee06de1993f6ea0d4ecfac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476582"
---
# <span data-ttu-id="b3e35-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="b3e35-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="b3e35-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3e35-102">SYNOPSIS</span></span>
<span data-ttu-id="b3e35-103">Erstellt eine Server Verwaltungssitzung.</span><span class="sxs-lookup"><span data-stu-id="b3e35-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3e35-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3e35-104">SYNTAX</span></span>

### <span data-ttu-id="b3e35-105">ByName</span><span class="sxs-lookup"><span data-stu-id="b3e35-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3e35-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="b3e35-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3e35-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3e35-107">DESCRIPTION</span></span>
<span data-ttu-id="b3e35-108">Das Cmdlet **New-AzureRmServerManagementSession** erstellt eine Azure Server Management-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b3e35-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="b3e35-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3e35-109">EXAMPLES</span></span>

## <span data-ttu-id="b3e35-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3e35-110">PARAMETERS</span></span>

### <span data-ttu-id="b3e35-111">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="b3e35-111">-Credential</span></span>
<span data-ttu-id="b3e35-112">Gibt ein **PSCredential** -Objekt für die Verbindung mit der Server Verwaltungssitzung an.</span><span class="sxs-lookup"><span data-stu-id="b3e35-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="b3e35-113">Verwenden Sie das Get-Credential-Cmdlet, um ein Anmeldeinformationsobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b3e35-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="b3e35-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b3e35-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3e35-115">-DefaultProfile</span></span>
<span data-ttu-id="b3e35-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3e35-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3e35-117">-Node</span><span class="sxs-lookup"><span data-stu-id="b3e35-117">-Node</span></span>
<span data-ttu-id="b3e35-118">Gibt den Knoten an, für den dieses Cmdlet die Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3e35-118">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="b3e35-119">Dieser Parameter kann anstelle der *ResourceGroupName* -und *NodeName* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3e35-119">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e35-120">-Nodename</span><span class="sxs-lookup"><span data-stu-id="b3e35-120">-NodeName</span></span>
<span data-ttu-id="b3e35-121">Gibt den Namen des Knotens an, für den dieses Cmdlet eine Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3e35-121">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3e35-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3e35-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3e35-123">Gibt die Ressourcengruppe des Knotens an, für den dieses Cmdlet eine Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b3e35-123">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e35-124">-Sitzungsname</span><span class="sxs-lookup"><span data-stu-id="b3e35-124">-SessionName</span></span>
<span data-ttu-id="b3e35-125">Gibt den Namen an, der für die Sitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3e35-125">Specifies the name to use for the session.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3e35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3e35-126">CommonParameters</span></span>
<span data-ttu-id="b3e35-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3e35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3e35-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3e35-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3e35-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3e35-129">INPUTS</span></span>

### <span data-ttu-id="b3e35-130">Knoten</span><span class="sxs-lookup"><span data-stu-id="b3e35-130">Node</span></span>
<span data-ttu-id="b3e35-131">Der Parameter "Node" akzeptiert den Wert vom Typ "Node" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b3e35-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="b3e35-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3e35-132">OUTPUTS</span></span>

### <span data-ttu-id="b3e35-133">Microsoft. Azure. Commands. Servermanagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="b3e35-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="b3e35-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3e35-134">NOTES</span></span>

## <span data-ttu-id="b3e35-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3e35-135">RELATED LINKS</span></span>

