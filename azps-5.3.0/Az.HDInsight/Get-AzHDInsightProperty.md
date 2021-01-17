---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469672"
---
# <span data-ttu-id="d7eaf-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="d7eaf-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="d7eaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="d7eaf-103">Ruft Eigenschaften zum Dienst HDInsight ab, z. B. verfügbare Standorte und Kapazität.</span><span class="sxs-lookup"><span data-stu-id="d7eaf-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="d7eaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7eaf-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7eaf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d7eaf-105">DESCRIPTION</span></span>
<span data-ttu-id="d7eaf-106">Das **Cmdlet "Get-AzHDInsightProperty"** ruft Eigenschaften ab, die für Azure HDInsight spezifisch sind, z. B. die Liste der verfügbaren Standorte, Versionen des HDInsight-Cluster und die verfügbare Rechenkapazität.</span><span class="sxs-lookup"><span data-stu-id="d7eaf-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="d7eaf-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d7eaf-107">EXAMPLES</span></span>

### <span data-ttu-id="d7eaf-108">Beispiel 1: Erhalten der Eigenschaften eines Azure -HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="d7eaf-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="d7eaf-109">Dieser Befehl ruft Eigenschaften eines HdInsight-Diensts vom Standort Ost US 2 ab.</span><span class="sxs-lookup"><span data-stu-id="d7eaf-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="d7eaf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7eaf-110">PARAMETERS</span></span>

### <span data-ttu-id="d7eaf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7eaf-111">-DefaultProfile</span></span>
<span data-ttu-id="d7eaf-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d7eaf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7eaf-113">-Location</span><span class="sxs-lookup"><span data-stu-id="d7eaf-113">-Location</span></span>
<span data-ttu-id="d7eaf-114">Gibt den Ort an, an dem die Eigenschaften von "HDInsight" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d7eaf-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="d7eaf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7eaf-115">CommonParameters</span></span>
<span data-ttu-id="d7eaf-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7eaf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7eaf-117">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7eaf-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7eaf-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d7eaf-118">INPUTS</span></span>

### <span data-ttu-id="d7eaf-119">Keine</span><span class="sxs-lookup"><span data-stu-id="d7eaf-119">None</span></span>
## <span data-ttu-id="d7eaf-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d7eaf-120">OUTPUTS</span></span>

### <span data-ttu-id="d7eaf-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="d7eaf-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="d7eaf-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d7eaf-122">NOTES</span></span>

## <span data-ttu-id="d7eaf-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d7eaf-123">RELATED LINKS</span></span>
