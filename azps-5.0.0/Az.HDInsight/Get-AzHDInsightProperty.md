---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296349"
---
# <span data-ttu-id="e80fa-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="e80fa-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="e80fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e80fa-102">SYNOPSIS</span></span>
<span data-ttu-id="e80fa-103">Ruft Eigenschaften des HDInsight-Diensts ab, beispielsweise Verfügbare Speicherorte und Kapazität.</span><span class="sxs-lookup"><span data-stu-id="e80fa-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="e80fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e80fa-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e80fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e80fa-105">DESCRIPTION</span></span>
<span data-ttu-id="e80fa-106">Das Cmdlet " **Get-AzHDInsightProperty** " ruft spezifische Eigenschaften für Azure-HDInsight ab, beispielsweise die Liste der verfügbaren Speicherorte, HDInsight-Cluster Versionen und die verfügbare Rechenkapazität.</span><span class="sxs-lookup"><span data-stu-id="e80fa-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="e80fa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e80fa-107">EXAMPLES</span></span>

### <span data-ttu-id="e80fa-108">Beispiel 1: Abrufen der Eigenschaften eines Azure HDInsight-Clusters</span><span class="sxs-lookup"><span data-stu-id="e80fa-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="e80fa-109">Dieser Befehl ruft Eigenschaften aus einem HDInsight-Dienst vom Standort East US 2 ab.</span><span class="sxs-lookup"><span data-stu-id="e80fa-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="e80fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e80fa-110">PARAMETERS</span></span>

### <span data-ttu-id="e80fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e80fa-111">-DefaultProfile</span></span>
<span data-ttu-id="e80fa-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e80fa-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e80fa-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="e80fa-113">-Location</span></span>
<span data-ttu-id="e80fa-114">Gibt den Speicherort an, für den HDInsight-Eigenschaften abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e80fa-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="e80fa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e80fa-115">CommonParameters</span></span>
<span data-ttu-id="e80fa-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e80fa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e80fa-117">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e80fa-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e80fa-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e80fa-118">INPUTS</span></span>

### <span data-ttu-id="e80fa-119">Keine</span><span class="sxs-lookup"><span data-stu-id="e80fa-119">None</span></span>
## <span data-ttu-id="e80fa-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e80fa-120">OUTPUTS</span></span>

### <span data-ttu-id="e80fa-121">Microsoft. Azure. Management. HDInsight. Models. AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="e80fa-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="e80fa-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="e80fa-122">NOTES</span></span>

## <span data-ttu-id="e80fa-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e80fa-123">RELATED LINKS</span></span>
