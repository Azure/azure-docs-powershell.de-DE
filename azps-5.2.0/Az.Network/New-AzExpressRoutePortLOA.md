---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303080"
---
# <span data-ttu-id="e6535-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="e6535-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="e6535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6535-102">SYNOPSIS</span></span>
<span data-ttu-id="e6535-103">Laden Sie das Autorisierungsschreiben für einen Expressroutenport herunter.</span><span class="sxs-lookup"><span data-stu-id="e6535-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="e6535-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e6535-104">SYNTAX</span></span>

### <span data-ttu-id="e6535-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e6535-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6535-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6535-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6535-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6535-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6535-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e6535-108">DESCRIPTION</span></span>
<span data-ttu-id="e6535-109">New-AzExpressRoutePortLOA Cmdlet lädt ein Autorisierungsdokument im PDF-Format für einen Expressroutenport herunter.</span><span class="sxs-lookup"><span data-stu-id="e6535-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="e6535-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e6535-110">EXAMPLES</span></span>

### <span data-ttu-id="e6535-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e6535-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="e6535-112">Laden Sie das Autorisierungsschreiben für den Expressroutenport "myPort" herunter, und speichern Sie es in der Datei "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="e6535-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="e6535-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6535-113">PARAMETERS</span></span>

### <span data-ttu-id="e6535-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6535-114">-AsJob</span></span>
<span data-ttu-id="e6535-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e6535-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6535-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="e6535-116">-CustomerName</span></span>
<span data-ttu-id="e6535-117">Der Name des Kunden, dem dieser Expressroutenport zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e6535-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="e6535-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6535-118">-DefaultProfile</span></span>
<span data-ttu-id="e6535-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6535-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6535-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="e6535-120">-Destination</span></span>
<span data-ttu-id="e6535-121">Der Ausgabedateipfad zum Speichern des Genehmigungsschreibens.</span><span class="sxs-lookup"><span data-stu-id="e6535-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="e6535-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="e6535-122">-ExpressRoutePort</span></span>
<span data-ttu-id="e6535-123">Die Expressroutenportressource.</span><span class="sxs-lookup"><span data-stu-id="e6535-123">The express route port resource.</span></span>

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

### <span data-ttu-id="e6535-124">-ID</span><span class="sxs-lookup"><span data-stu-id="e6535-124">-Id</span></span>
<span data-ttu-id="e6535-125">ResourceId des Expressroutenports.</span><span class="sxs-lookup"><span data-stu-id="e6535-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="e6535-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6535-126">-PassThru</span></span>
<span data-ttu-id="e6535-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e6535-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e6535-128">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e6535-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6535-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="e6535-129">-PortName</span></span>
<span data-ttu-id="e6535-130">Der Name des Expressroutenports.</span><span class="sxs-lookup"><span data-stu-id="e6535-130">The express route port name.</span></span>

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

### <span data-ttu-id="e6535-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6535-131">-ResourceGroupName</span></span>
<span data-ttu-id="e6535-132">Der Ressourcengruppenname des Expressroutenports.</span><span class="sxs-lookup"><span data-stu-id="e6535-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="e6535-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6535-133">CommonParameters</span></span>
<span data-ttu-id="e6535-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6535-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6535-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6535-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6535-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e6535-136">INPUTS</span></span>

### <span data-ttu-id="e6535-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e6535-137">System.String</span></span>

## <span data-ttu-id="e6535-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e6535-138">OUTPUTS</span></span>

### <span data-ttu-id="e6535-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6535-139">System.Boolean</span></span>

## <span data-ttu-id="e6535-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e6535-140">NOTES</span></span>

## <span data-ttu-id="e6535-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e6535-141">RELATED LINKS</span></span>
