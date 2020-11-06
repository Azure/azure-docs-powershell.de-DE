---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/test-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Test-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: 7f47d800fd0eab51edae321f9d21260f50075b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482609"
---
# <span data-ttu-id="4045a-101">Test-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4045a-101">Test-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="4045a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4045a-102">SYNOPSIS</span></span>
<span data-ttu-id="4045a-103">Testet das vorhanden sein einer Instanz des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="4045a-103">Tests the existence of an instance of Analysis Services server</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4045a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4045a-104">SYNTAX</span></span>

```
Test-AzureRmAnalysisServicesServer [-Name] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4045a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4045a-105">DESCRIPTION</span></span>
<span data-ttu-id="4045a-106">Das Test-AzureRmAnalysisServicesServer-Cmdlet testet das vorhanden sein einer Instanz des Analysis Services-Servers.</span><span class="sxs-lookup"><span data-stu-id="4045a-106">The Test-AzureRmAnalysisServicesServer cmdlet tests the existence of an instance of Analysis Services server</span></span>

## <span data-ttu-id="4045a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4045a-107">EXAMPLES</span></span>

### <span data-ttu-id="4045a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4045a-108">Example 1</span></span>
```
PS C:\> Test-AzureRmAnalysisServicesServer -Name "testserver" -ResourceGroupName "testgroup"
```

<span data-ttu-id="4045a-109">Dieser Befehl testet, ob ein Server mit dem Namen "Testserver" in der testgroup der ResourceGroup vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4045a-109">This command will test if there is a server named testserver in the resourcegroup testgroup</span></span>

## <span data-ttu-id="4045a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4045a-110">PARAMETERS</span></span>

### <span data-ttu-id="4045a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4045a-111">-DefaultProfile</span></span>
<span data-ttu-id="4045a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4045a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4045a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4045a-113">-Name</span></span>
<span data-ttu-id="4045a-114">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="4045a-114">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="4045a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4045a-115">-ResourceGroupName</span></span>
<span data-ttu-id="4045a-116">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="4045a-116">Name of the Azure resource group to which the server belongs</span></span>

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

### <span data-ttu-id="4045a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4045a-117">CommonParameters</span></span>
<span data-ttu-id="4045a-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4045a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4045a-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4045a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4045a-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4045a-120">INPUTS</span></span>

### <span data-ttu-id="4045a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="4045a-121">System.String</span></span>

## <span data-ttu-id="4045a-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4045a-122">OUTPUTS</span></span>

### <span data-ttu-id="4045a-123">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4045a-123">System.Boolean</span></span>

## <span data-ttu-id="4045a-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="4045a-124">NOTES</span></span>
<span data-ttu-id="4045a-125">Alias: Test-AzureAs</span><span class="sxs-lookup"><span data-stu-id="4045a-125">Alias: Test-AzureAs</span></span>

## <span data-ttu-id="4045a-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4045a-126">RELATED LINKS</span></span>

[<span data-ttu-id="4045a-127">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4045a-127">Get-AzureRmAnalysisServicesServer</span></span>](./Get-AzureRmAnalysisServicesServer.md)

[<span data-ttu-id="4045a-128">Remove-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="4045a-128">Remove-AzureRmAnalysisServicesServer</span></span>](./Remove-AzureRmAnalysisServicesServer.md)
