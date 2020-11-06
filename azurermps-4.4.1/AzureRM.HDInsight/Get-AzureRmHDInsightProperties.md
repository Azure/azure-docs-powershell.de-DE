---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: e1701d60289343bb61a2891617fd10c6b9987b6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504994"
---
# <span data-ttu-id="a28e7-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="a28e7-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="a28e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a28e7-102">SYNOPSIS</span></span>
<span data-ttu-id="a28e7-103">Ruft Eigenschaften des HDInsight-Diensts ab, beispielsweise Verfügbare Speicherorte und Kapazität.</span><span class="sxs-lookup"><span data-stu-id="a28e7-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a28e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a28e7-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a28e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a28e7-105">DESCRIPTION</span></span>
<span data-ttu-id="a28e7-106">Das Cmdlet " **Get-AzureRmHDInsightProperties** " ruft spezifische Eigenschaften für Azure-HDInsight ab, beispielsweise die Liste der verfügbaren Speicherorte, HDInsight-Cluster Versionen und die verfügbare Rechenkapazität.</span><span class="sxs-lookup"><span data-stu-id="a28e7-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="a28e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a28e7-107">EXAMPLES</span></span>

### <span data-ttu-id="a28e7-108">Beispiel 1: Abrufen der Eigenschaften eines Azure HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="a28e7-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="a28e7-109">Dieser Befehl ruft Eigenschaften aus einem HDInsight-Dienst vom Standort East US 2 ab.</span><span class="sxs-lookup"><span data-stu-id="a28e7-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="a28e7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a28e7-110">PARAMETERS</span></span>

### <span data-ttu-id="a28e7-111">-Standort</span><span class="sxs-lookup"><span data-stu-id="a28e7-111">-Location</span></span>
<span data-ttu-id="a28e7-112">Gibt den Speicherort an, für den HDInsight-Eigenschaften abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a28e7-112">Specifies the location for which to fetch HDInsight properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a28e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28e7-113">-DefaultProfile</span></span>
<span data-ttu-id="a28e7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a28e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a28e7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28e7-115">CommonParameters</span></span>
<span data-ttu-id="a28e7-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a28e7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28e7-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a28e7-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28e7-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a28e7-118">INPUTS</span></span>

## <span data-ttu-id="a28e7-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a28e7-119">OUTPUTS</span></span>

### <span data-ttu-id="a28e7-120">Microsoft. Azure. Management. HDInsight. Models. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="a28e7-120">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="a28e7-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="a28e7-121">NOTES</span></span>

## <span data-ttu-id="a28e7-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a28e7-122">RELATED LINKS</span></span>

