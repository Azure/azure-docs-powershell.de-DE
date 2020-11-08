---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/test-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Test-AzAnalysisServicesServer.md
ms.openlocfilehash: 86a82d5c82cdb775e7b07c6189244e494d14c4a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009473"
---
# <span data-ttu-id="ebc9d-101">Test-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ebc9d-101">Test-AzAnalysisServicesServer</span></span>

## <span data-ttu-id="ebc9d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ebc9d-102">SYNOPSIS</span></span>
<span data-ttu-id="ebc9d-103">Testet das vorhanden sein einer Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="ebc9d-103">Tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="ebc9d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebc9d-104">SYNTAX</span></span>

```
Test-AzAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebc9d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebc9d-105">DESCRIPTION</span></span>
<span data-ttu-id="ebc9d-106">Das Test-AzAnalysisServicesServer-Cmdlet testet das vorhanden sein einer Instanz des Analysis Services-Servers.</span><span class="sxs-lookup"><span data-stu-id="ebc9d-106">The Test-AzAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="ebc9d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebc9d-107">EXAMPLES</span></span>

### <span data-ttu-id="ebc9d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ebc9d-108">Example 1</span></span>
```
PS C:\> Test-AzAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="ebc9d-109">Dieser Befehl testet, ob ein Server mit dem Namen "Testserver" in der testgroup der ResourceGroup vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ebc9d-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="ebc9d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebc9d-110">PARAMETERS</span></span>

### <span data-ttu-id="ebc9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebc9d-111">-DefaultProfile</span></span>
<span data-ttu-id="ebc9d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebc9d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebc9d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ebc9d-113">-Name</span></span>
<span data-ttu-id="ebc9d-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="ebc9d-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="ebc9d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebc9d-115">-ResourceGroupName</span></span>
<span data-ttu-id="ebc9d-116">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="ebc9d-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="ebc9d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebc9d-117">CommonParameters</span></span>
<span data-ttu-id="ebc9d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebc9d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebc9d-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebc9d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebc9d-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ebc9d-120">INPUTS</span></span>

### <span data-ttu-id="ebc9d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ebc9d-121">System.String</span></span>

## <span data-ttu-id="ebc9d-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ebc9d-122">OUTPUTS</span></span>

### <span data-ttu-id="ebc9d-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ebc9d-123">System.Boolean</span></span>

## <span data-ttu-id="ebc9d-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="ebc9d-124">NOTES</span></span>
<span data-ttu-id="ebc9d-125">Alias: Test-AzAs</span><span class="sxs-lookup"><span data-stu-id="ebc9d-125">Alias: Test-AzAs</span></span>

## <span data-ttu-id="ebc9d-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ebc9d-126">RELATED LINKS</span></span>

[<span data-ttu-id="ebc9d-127">Get-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ebc9d-127">Get-AzAnalysisServicesServer</span></span>](./Get-AzAnalysisServicesServer.md)

[<span data-ttu-id="ebc9d-128">Remove-AzAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="ebc9d-128">Remove-AzAnalysisServicesServer</span></span>](./Remove-AzAnalysisServicesServer.md)
