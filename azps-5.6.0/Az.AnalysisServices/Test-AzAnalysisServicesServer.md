---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: cb6680276359fddcf9a98cde3e90cb44185c4e85
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922219"
---
# <span data-ttu-id="743ca-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="743ca-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="743ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="743ca-102">SYNOPSIS</span></span>
<span data-ttu-id="743ca-103">Testet das Vorhandensein einer Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="743ca-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="743ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="743ca-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="743ca-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="743ca-105">DESCRIPTION</span></span>
<span data-ttu-id="743ca-106">Das Test-AzAnalysisServicesServer-Cmdlet testet das Vorhandensein einer Instanz des Analysis Services-Servers.</span><span class="sxs-lookup"><span data-stu-id="743ca-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="743ca-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="743ca-107">EXAMPLES</span></span>

### <span data-ttu-id="743ca-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="743ca-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="743ca-109">Dieser Befehl testt, ob in der Ressourcengruppentestgruppe ein Server namens Testserver vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="743ca-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="743ca-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="743ca-110">PARAMETERS</span></span>

### <span data-ttu-id="743ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="743ca-111">-DefaultProfile</span></span>
<span data-ttu-id="743ca-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="743ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="743ca-113">-Name</span><span class="sxs-lookup"><span data-stu-id="743ca-113">-Name</span></span>
<span data-ttu-id="743ca-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="743ca-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="743ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="743ca-115">-ResourceGroupName</span></span>
<span data-ttu-id="743ca-116">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="743ca-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="743ca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="743ca-117">CommonParameters</span></span>
<span data-ttu-id="743ca-118">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="743ca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="743ca-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="743ca-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="743ca-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="743ca-120">INPUTS</span></span>

### <span data-ttu-id="743ca-121">System.String</span><span class="sxs-lookup"><span data-stu-id="743ca-121">System.String</span></span>

## <span data-ttu-id="743ca-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="743ca-122">OUTPUTS</span></span>

### <span data-ttu-id="743ca-123">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="743ca-123">System.Boolean</span></span>

## <span data-ttu-id="743ca-124">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="743ca-124">NOTES</span></span>
<span data-ttu-id="743ca-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="743ca-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="743ca-126">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="743ca-126">RELATED LINKS</span></span>

[<span data-ttu-id="743ca-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="743ca-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="743ca-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="743ca-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
