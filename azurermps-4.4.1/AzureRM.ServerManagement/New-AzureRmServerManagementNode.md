---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: e77059b94f9311caf25b58f2d626f0cafc4657e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496870"
---
# <span data-ttu-id="a4c85-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="a4c85-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="a4c85-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a4c85-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c85-103">Erstellt einen Server Verwaltungsknoten.</span><span class="sxs-lookup"><span data-stu-id="a4c85-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4c85-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4c85-104">SYNTAX</span></span>

### <span data-ttu-id="a4c85-105">ByName</span><span class="sxs-lookup"><span data-stu-id="a4c85-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tags <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4c85-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a4c85-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4c85-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4c85-107">DESCRIPTION</span></span>
<span data-ttu-id="a4c85-108">Das Cmdlet **New-AzureRmServerManagementNode** erstellt einen Azure Server Management-Knoten.</span><span class="sxs-lookup"><span data-stu-id="a4c85-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="a4c85-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a4c85-109">EXAMPLES</span></span>

## <span data-ttu-id="a4c85-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4c85-110">PARAMETERS</span></span>

### <span data-ttu-id="a4c85-111">-Computername</span><span class="sxs-lookup"><span data-stu-id="a4c85-111">-ComputerName</span></span>
<span data-ttu-id="a4c85-112">Gibt den Computernamen des Computers an, der verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="a4c85-112">Specifies the computer name of the computer that is being managed.</span></span>

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

### <span data-ttu-id="a4c85-113">– Anmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="a4c85-113">-Credential</span></span>
<span data-ttu-id="a4c85-114">Gibt ein **PSCredential** -Objekt für die Verbindung mit dem Server Verwaltungsknoten an.</span><span class="sxs-lookup"><span data-stu-id="a4c85-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="a4c85-115">Verwenden Sie das Get-Credential-Cmdlet, um ein Anmeldeinformationsobjekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a4c85-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="a4c85-116">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a4c85-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4c85-117">-Gateway</span><span class="sxs-lookup"><span data-stu-id="a4c85-117">-Gateway</span></span>
<span data-ttu-id="a4c85-118">Gibt das Gateway an, das den Knoten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a4c85-118">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="a4c85-119">Dieser Parameter kann anstelle der *ResourceGroupName* -, *GatewayName* -und *Location* -Parameter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a4c85-119">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4c85-120">-Gatewayname</span><span class="sxs-lookup"><span data-stu-id="a4c85-120">-GatewayName</span></span>
<span data-ttu-id="a4c85-121">Gibt den Namen des Gateways an, das auf den Knoten zugreift.</span><span class="sxs-lookup"><span data-stu-id="a4c85-121">Specifies the name of the gateway that accesses the node.</span></span>

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

### <span data-ttu-id="a4c85-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="a4c85-122">-Location</span></span>
<span data-ttu-id="a4c85-123">Gibt den Speicherort an, an dem dieses Cmdlet den Knoten erstellt.</span><span class="sxs-lookup"><span data-stu-id="a4c85-123">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4c85-124">-Nodename</span><span class="sxs-lookup"><span data-stu-id="a4c85-124">-NodeName</span></span>
<span data-ttu-id="a4c85-125">Gibt den Namen des Knotens an.</span><span class="sxs-lookup"><span data-stu-id="a4c85-125">Specifies the name of the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4c85-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c85-126">-ResourceGroupName</span></span>
<span data-ttu-id="a4c85-127">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet den Knoten erstellt.</span><span class="sxs-lookup"><span data-stu-id="a4c85-127">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="a4c85-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="a4c85-128">-Tags</span></span>
<span data-ttu-id="a4c85-129">Gibt Tags als Schlüssel-Wert-Paare an.</span><span class="sxs-lookup"><span data-stu-id="a4c85-129">Specifies tags as key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4c85-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c85-130">-DefaultProfile</span></span>
<span data-ttu-id="a4c85-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a4c85-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4c85-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c85-132">CommonParameters</span></span>
<span data-ttu-id="a4c85-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c85-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c85-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4c85-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c85-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a4c85-135">INPUTS</span></span>

### <span data-ttu-id="a4c85-136">Gateway</span><span class="sxs-lookup"><span data-stu-id="a4c85-136">Gateway</span></span>
<span data-ttu-id="a4c85-137">Der Parameter "Gateway" akzeptiert den Wert vom Typ "Gateway" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a4c85-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="a4c85-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a4c85-138">OUTPUTS</span></span>

### <span data-ttu-id="a4c85-139">Microsoft. Azure. Commands. Servermanagement. Modell. Node</span><span class="sxs-lookup"><span data-stu-id="a4c85-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="a4c85-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="a4c85-140">NOTES</span></span>

## <span data-ttu-id="a4c85-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a4c85-141">RELATED LINKS</span></span>

[<span data-ttu-id="a4c85-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="a4c85-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="a4c85-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="a4c85-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


