---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/get-azurermanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/Get-AzureRmAnalysisServicesServer.md
ms.openlocfilehash: f67c22b483b561af8ffcf2ede9bc1e489379c0d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663499"
---
# <span data-ttu-id="7d8c1-101">Get-AzureRmAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d8c1-101">Get-AzureRmAnalysisServicesServer</span></span>

## <span data-ttu-id="7d8c1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8c1-103">Ruft die Details eines Analysis Services-Servers ab.</span><span class="sxs-lookup"><span data-stu-id="7d8c1-103">Gets the details of an Analysis Services server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d8c1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d8c1-104">SYNTAX</span></span>

```
Get-AzureRmAnalysisServicesServer [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d8c1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d8c1-105">DESCRIPTION</span></span>
<span data-ttu-id="7d8c1-106">Das Get-AzureRmAnalysisServicesServer-Cmdlet ruft die Details eines Analysis Services-Servers ab.</span><span class="sxs-lookup"><span data-stu-id="7d8c1-106">The Get-AzureRmAnalysisServicesServer cmdlet gets the details of an Analysis Services server.</span></span>

## <span data-ttu-id="7d8c1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d8c1-107">EXAMPLES</span></span>

### <span data-ttu-id="7d8c1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7d8c1-108">Example 1</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03"
```

<span data-ttu-id="7d8c1-109">Dieser Befehl ruft alle Azure Analysis Services-Server in der Ressourcengruppe mit dem Namen ResourceGroup03 ab.</span><span class="sxs-lookup"><span data-stu-id="7d8c1-109">This command gets all Azure Analysis Services servers in the resource group named ResourceGroup03.</span></span>

### <span data-ttu-id="7d8c1-110">Beispiel 2: Abrufen eines Servers</span><span class="sxs-lookup"><span data-stu-id="7d8c1-110">Example 2: Get a server</span></span>
```
PS C:\>Get-AzureRmAnalysisServicesServer -ResourceGroupName "ResourceGroup03" -Name "testserver"
```

<span data-ttu-id="7d8c1-111">Mit diesem Befehl wird der Azure Analysis Services-Server mit dem Namen Testserver in der Ressourcengruppe mit dem Namen ResourceGroup03 abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7d8c1-111">This command gets the Azure Analysis Services server named testserver in the resource group named ResourceGroup03.</span></span>

## <span data-ttu-id="7d8c1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d8c1-112">PARAMETERS</span></span>

### <span data-ttu-id="7d8c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8c1-113">-DefaultProfile</span></span>
<span data-ttu-id="7d8c1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d8c1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d8c1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7d8c1-115">-Name</span></span>
<span data-ttu-id="7d8c1-116">Name des Analysis Services-Servers</span><span class="sxs-lookup"><span data-stu-id="7d8c1-116">Name of the Analysis Services server</span></span>

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

### <span data-ttu-id="7d8c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="7d8c1-118">Name der Azure-Ressourcengruppe, zu der der Server gehört</span><span class="sxs-lookup"><span data-stu-id="7d8c1-118">Name of the Azure resource group to which the server belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d8c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8c1-119">CommonParameters</span></span>
<span data-ttu-id="7d8c1-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8c1-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d8c1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8c1-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d8c1-122">INPUTS</span></span>

### <span data-ttu-id="7d8c1-123">Keine</span><span class="sxs-lookup"><span data-stu-id="7d8c1-123">None</span></span>
<span data-ttu-id="7d8c1-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7d8c1-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d8c1-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d8c1-125">OUTPUTS</span></span>

### <span data-ttu-id="7d8c1-126">Microsoft. Azure. Commands. AnalysisServices. Models. AzureAnalysisServicesServer</span><span class="sxs-lookup"><span data-stu-id="7d8c1-126">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesServer</span></span>

## <span data-ttu-id="7d8c1-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d8c1-127">NOTES</span></span>
<span data-ttu-id="7d8c1-128">Alias: Get-AzureAs</span><span class="sxs-lookup"><span data-stu-id="7d8c1-128">Alias: Get-AzureAs</span></span>

## <span data-ttu-id="7d8c1-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d8c1-129">RELATED LINKS</span></span>

[<span data-ttu-id="7d8c1-130">Neu – AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="7d8c1-130">New-AzureRmAnalysisServicesServer </span></span>](./New-AzureRmAnalysisServicesServer .md)

[<span data-ttu-id="7d8c1-131">Remove-AzureRmAnalysisServicesServer </span><span class="sxs-lookup"><span data-stu-id="7d8c1-131">Remove-AzureRmAnalysisServicesServer </span></span>](./Remove-AzureRmAnalysisServicesServer .md)
