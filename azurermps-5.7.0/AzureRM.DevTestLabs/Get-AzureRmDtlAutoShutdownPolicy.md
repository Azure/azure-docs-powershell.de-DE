---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: 557cfcaefef1a85fe7ad0a8bd62f4ddbf0ecb6f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481233"
---
# <span data-ttu-id="8c126-101">Get-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="8c126-101">Get-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="8c126-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c126-102">SYNOPSIS</span></span>
<span data-ttu-id="8c126-103">Ruft die Richtlinie für das automatische Herunterfahren einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="8c126-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c126-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c126-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c126-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c126-105">DESCRIPTION</span></span>
<span data-ttu-id="8c126-106">Das Cmdlet " **Get-AzureRmDtlAutoShutdownPolicy** " Ruft die Richtlinie für das automatische Herunterfahren einer Übungseinheit ab, mit der Sie alle virtuellen Computer in einer Übungseinheit automatisch zu einer bestimmten Tageszeit Herunterfahren können.</span><span class="sxs-lookup"><span data-stu-id="8c126-106">The **Get-AzureRmDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="8c126-107">Das Cmdlet gibt zurück, ob der Status der Richtlinie aktiviert ist, und die Tageszeit, die Sie festgelegt haben, um die virtuellen Lab-Computer automatisch herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="8c126-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="8c126-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c126-108">EXAMPLES</span></span>

## <span data-ttu-id="8c126-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c126-109">PARAMETERS</span></span>

### <span data-ttu-id="8c126-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c126-110">-DefaultProfile</span></span>
<span data-ttu-id="8c126-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8c126-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c126-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="8c126-112">-LabName</span></span>
<span data-ttu-id="8c126-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für das automatische Herunterfahren erhält.</span><span class="sxs-lookup"><span data-stu-id="8c126-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="8c126-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c126-114">-ResourceGroupName</span></span>
<span data-ttu-id="8c126-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="8c126-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c126-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c126-116">CommonParameters</span></span>
<span data-ttu-id="8c126-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c126-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c126-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c126-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c126-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c126-119">INPUTS</span></span>

### <span data-ttu-id="8c126-120">Keine</span><span class="sxs-lookup"><span data-stu-id="8c126-120">None</span></span>
<span data-ttu-id="8c126-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8c126-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8c126-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c126-122">OUTPUTS</span></span>

### <span data-ttu-id="8c126-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="8c126-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="8c126-124">Dieses Cmdlet gibt den Zeitplan zurück, der angibt, wann die virtuellen Computer der Übungseinheit heruntergefahren werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8c126-124">This cmdlet returns the schedule which specifies when the lab's virtual machines must shut down.</span></span>

## <span data-ttu-id="8c126-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c126-125">NOTES</span></span>

## <span data-ttu-id="8c126-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c126-126">RELATED LINKS</span></span>

[<span data-ttu-id="8c126-127">Satz-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="8c126-127">Set-AzureRmDtlAutoShutdownPolicy</span></span>](./Set-AzureRmDtlAutoShutdownPolicy.md)


