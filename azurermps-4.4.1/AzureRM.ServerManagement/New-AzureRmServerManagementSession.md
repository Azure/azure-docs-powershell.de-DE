---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 0ae3e221ee39a00381f009f45a9a2f508a552b6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481605"
---
# <span data-ttu-id="f22f8-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="f22f8-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="f22f8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f22f8-102">SYNOPSIS</span></span>
<span data-ttu-id="f22f8-103">Erstellt eine Server Verwaltungssitzung.</span><span class="sxs-lookup"><span data-stu-id="f22f8-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f22f8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f22f8-104">SYNTAX</span></span>

### <span data-ttu-id="f22f8-105">ByName</span><span class="sxs-lookup"><span data-stu-id="f22f8-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f22f8-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="f22f8-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f22f8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f22f8-107">DESCRIPTION</span></span>
<span data-ttu-id="f22f8-108">Das Cmdlet **New-AzureRmServerManagementSession** erstellt eine Azure Server Management-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f22f8-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="f22f8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f22f8-109">EXAMPLES</span></span>

## <span data-ttu-id="f22f8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f22f8-110">PARAMETERS</span></span>

### <span data-ttu-id="f22f8-111">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="f22f8-111">-Credential</span></span>
<span data-ttu-id="f22f8-112">Gibt ein **PSCredential** -Objekt für die Verbindung mit der Server Verwaltungssitzung an.</span><span class="sxs-lookup"><span data-stu-id="f22f8-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="f22f8-113">Verwenden Sie das Get-Credential-Cmdlet, um ein Anmeldeinformationsobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f22f8-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="f22f8-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="f22f8-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22f8-115">-Node</span><span class="sxs-lookup"><span data-stu-id="f22f8-115">-Node</span></span>
<span data-ttu-id="f22f8-116">Gibt den Knoten an, für den dieses Cmdlet die Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="f22f8-116">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="f22f8-117">Dieser Parameter kann anstelle der *ResourceGroupName* -und *NodeName* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f22f8-117">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

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

### <span data-ttu-id="f22f8-118">-Nodename</span><span class="sxs-lookup"><span data-stu-id="f22f8-118">-NodeName</span></span>
<span data-ttu-id="f22f8-119">Gibt den Namen des Knotens an, für den dieses Cmdlet eine Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="f22f8-119">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f22f8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22f8-120">-ResourceGroupName</span></span>
<span data-ttu-id="f22f8-121">Gibt die Ressourcengruppe des Knotens an, für den dieses Cmdlet eine Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="f22f8-121">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

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

### <span data-ttu-id="f22f8-122">-Sitzungsname</span><span class="sxs-lookup"><span data-stu-id="f22f8-122">-SessionName</span></span>
<span data-ttu-id="f22f8-123">Gibt den Namen an, der für die Sitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f22f8-123">Specifies the name to use for the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f22f8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22f8-124">-DefaultProfile</span></span>
<span data-ttu-id="f22f8-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f22f8-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f22f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22f8-126">CommonParameters</span></span>
<span data-ttu-id="f22f8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f22f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22f8-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f22f8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22f8-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f22f8-129">INPUTS</span></span>

### <span data-ttu-id="f22f8-130">Knoten</span><span class="sxs-lookup"><span data-stu-id="f22f8-130">Node</span></span>
<span data-ttu-id="f22f8-131">Der Parameter "Node" akzeptiert den Wert vom Typ "Node" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f22f8-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="f22f8-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f22f8-132">OUTPUTS</span></span>

### <span data-ttu-id="f22f8-133">Microsoft. Azure. Commands. Servermanagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="f22f8-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="f22f8-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f22f8-134">NOTES</span></span>

## <span data-ttu-id="f22f8-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f22f8-135">RELATED LINKS</span></span>

