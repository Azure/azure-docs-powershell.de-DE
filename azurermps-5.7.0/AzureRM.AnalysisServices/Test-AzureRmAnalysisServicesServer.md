---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 9dd8a86d1e98268708d7b0a12448df109ee083f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504646"
---
# <span data-ttu-id="28b64-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="28b64-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="28b64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28b64-102">SYNOPSIS</span></span>
<span data-ttu-id="28b64-103">Testet das vorhanden sein einer Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="28b64-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28b64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28b64-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28b64-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28b64-105">DESCRIPTION</span></span>
<span data-ttu-id="28b64-106">Das Test-AzureRmAnalysisServicesServer-Cmdlet testet das vorhanden sein einer Instanz des Analysis Services-Servers.</span><span class="sxs-lookup"><span data-stu-id="28b64-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="28b64-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28b64-107">EXAMPLES</span></span>

### <span data-ttu-id="28b64-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28b64-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="28b64-109">Dieser Befehl testet, ob ein Server mit dem Namen "Testserver" in der testgroup der ResourceGroup vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="28b64-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="28b64-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="28b64-110">PARAMETERS</span></span>

### <span data-ttu-id="28b64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b64-111">-DefaultProfile</span></span>
<span data-ttu-id="28b64-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28b64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28b64-113">-Name</span><span class="sxs-lookup"><span data-stu-id="28b64-113">-Name</span></span>
<span data-ttu-id="28b64-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="28b64-114">Name of the Analysis Services server</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b64-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b64-115">-ResourceGroupName</span></span>
<span data-ttu-id="28b64-116">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="28b64-116">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b64-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b64-117">CommonParameters</span></span>
<span data-ttu-id="28b64-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b64-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b64-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b64-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b64-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28b64-120">INPUTS</span></span>

### <span data-ttu-id="28b64-121">Keine</span><span class="sxs-lookup"><span data-stu-id="28b64-121">None</span></span>
<span data-ttu-id="28b64-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="28b64-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28b64-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28b64-123">OUTPUTS</span></span>

### <span data-ttu-id="28b64-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="28b64-124">System.Boolean</span></span>

## <span data-ttu-id="28b64-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="28b64-125">NOTES</span></span>
<span data-ttu-id="28b64-126">Alias: Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="28b64-126">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="28b64-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28b64-127">RELATED LINKS</span></span>

[<span data-ttu-id="28b64-128">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="28b64-128">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="28b64-129">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="28b64-129">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
