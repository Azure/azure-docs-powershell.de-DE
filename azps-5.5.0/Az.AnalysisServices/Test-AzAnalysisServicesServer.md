---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171959"
---
# <span data-ttu-id="6fb52-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6fb52-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="6fb52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fb52-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb52-103">Überprüft das Vorhandensein einer Instanz des Analysis Services-Servers.</span><span class="sxs-lookup"><span data-stu-id="6fb52-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="6fb52-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fb52-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fb52-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fb52-105">DESCRIPTION</span></span>
<span data-ttu-id="6fb52-106">Das Test-AzAnalysisServicesServer cmdlet überprüft das Vorhandensein einer Instanz des Analysis Services-Servers.</span><span class="sxs-lookup"><span data-stu-id="6fb52-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="6fb52-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6fb52-107">EXAMPLES</span></span>

### <span data-ttu-id="6fb52-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6fb52-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="6fb52-109">Dieser Befehl testt, ob die Testgruppe der Ressourcengruppe einen Server mit dem Namen "Testserver" hat.</span><span class="sxs-lookup"><span data-stu-id="6fb52-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="6fb52-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fb52-110">PARAMETERS</span></span>

### <span data-ttu-id="6fb52-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb52-111">-DefaultProfile</span></span>
<span data-ttu-id="6fb52-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6fb52-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fb52-113">-Name</span><span class="sxs-lookup"><span data-stu-id="6fb52-113">-Name</span></span>
<span data-ttu-id="6fb52-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="6fb52-114">Name of the Analysis Services server</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb52-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb52-115">-ResourceGroupName</span></span>
<span data-ttu-id="6fb52-116">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="6fb52-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fb52-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb52-117">CommonParameters</span></span>
<span data-ttu-id="6fb52-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb52-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb52-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb52-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb52-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6fb52-120">INPUTS</span></span>

### <span data-ttu-id="6fb52-121">System.String</span><span class="sxs-lookup"><span data-stu-id="6fb52-121">System.String</span></span>

## <span data-ttu-id="6fb52-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6fb52-122">OUTPUTS</span></span>

### <span data-ttu-id="6fb52-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6fb52-123">System.Boolean</span></span>

## <span data-ttu-id="6fb52-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6fb52-124">NOTES</span></span>
<span data-ttu-id="6fb52-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="6fb52-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="6fb52-126">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6fb52-126">RELATED LINKS</span></span>

[<span data-ttu-id="6fb52-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6fb52-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="6fb52-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="6fb52-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
