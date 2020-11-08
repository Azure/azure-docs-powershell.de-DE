---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175066"
---
# <span data-ttu-id="e008a-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="e008a-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="e008a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e008a-102">SYNOPSIS</span></span>
<span data-ttu-id="e008a-103">Dokument zum Herunterladen des Autorisierungs Dokuments für einen Express-Route-Port</span><span class="sxs-lookup"><span data-stu-id="e008a-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="e008a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e008a-104">SYNTAX</span></span>

### <span data-ttu-id="e008a-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e008a-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e008a-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e008a-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e008a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e008a-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e008a-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e008a-108">DESCRIPTION</span></span>
<span data-ttu-id="e008a-109">New-AzExpressRoutePortLOA-Cmdlet lädt im PDF-Format einen Brief des Autorisierungs Dokuments für einen Express-Routen-Port herunter.</span><span class="sxs-lookup"><span data-stu-id="e008a-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="e008a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e008a-110">EXAMPLES</span></span>

### <span data-ttu-id="e008a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e008a-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="e008a-112">Laden Sie das Dokument für die Autorisierung für den Express-Routen-Port "myPort" herunter, und speichern Sie es in der Datei "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="e008a-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="e008a-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e008a-113">PARAMETERS</span></span>

### <span data-ttu-id="e008a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e008a-114">-AsJob</span></span>
<span data-ttu-id="e008a-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e008a-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e008a-116">-Kundenname</span><span class="sxs-lookup"><span data-stu-id="e008a-116">-CustomerName</span></span>
<span data-ttu-id="e008a-117">Der Name des Kunden, dem dieser Express-Route-Port zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e008a-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e008a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e008a-118">-DefaultProfile</span></span>
<span data-ttu-id="e008a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e008a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e008a-120">-Ziel</span><span class="sxs-lookup"><span data-stu-id="e008a-120">-Destination</span></span>
<span data-ttu-id="e008a-121">Der Ausgabe-Dateipfad, in dem der Autorisierungs Buchstabe gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e008a-121">The output filepath to store the Letter of Authorization to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e008a-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e008a-122">-ExpressRoutePort</span></span>
<span data-ttu-id="e008a-123">Die Express-Route-Port-Ressource.</span><span class="sxs-lookup"><span data-stu-id="e008a-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e008a-124">-ID</span><span class="sxs-lookup"><span data-stu-id="e008a-124">-Id</span></span>
<span data-ttu-id="e008a-125">Die Quelle des Express-Route-Ports.</span><span class="sxs-lookup"><span data-stu-id="e008a-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e008a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e008a-126">-PassThru</span></span>
<span data-ttu-id="e008a-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e008a-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e008a-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e008a-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e008a-129">-Portname</span><span class="sxs-lookup"><span data-stu-id="e008a-129">-PortName</span></span>
<span data-ttu-id="e008a-130">Der Name des Express-Route-Ports.</span><span class="sxs-lookup"><span data-stu-id="e008a-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e008a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e008a-131">-ResourceGroupName</span></span>
<span data-ttu-id="e008a-132">Der Name der Ressourcengruppe des Express Route-Ports.</span><span class="sxs-lookup"><span data-stu-id="e008a-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e008a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e008a-133">CommonParameters</span></span>
<span data-ttu-id="e008a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e008a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e008a-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e008a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e008a-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e008a-136">INPUTS</span></span>

### <span data-ttu-id="e008a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e008a-137">System.String</span></span>

## <span data-ttu-id="e008a-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e008a-138">OUTPUTS</span></span>

### <span data-ttu-id="e008a-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e008a-139">System.Boolean</span></span>

## <span data-ttu-id="e008a-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="e008a-140">NOTES</span></span>

## <span data-ttu-id="e008a-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e008a-141">RELATED LINKS</span></span>
