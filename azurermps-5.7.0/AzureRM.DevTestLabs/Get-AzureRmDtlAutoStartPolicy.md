---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAutoStartPolicy.md
ms.openlocfilehash: c61739c3bd80c5c5c15c7e10d8a787f45c44ec69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662739"
---
# <span data-ttu-id="f4a50-101">Get-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="f4a50-101">Get-AzureRmDtlAutoStartPolicy</span></span>

## <span data-ttu-id="f4a50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f4a50-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a50-103">Ruft die Richtlinie für den automatischen Start einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="f4a50-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4a50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4a50-104">SYNTAX</span></span>

```
Get-AzureRmDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4a50-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4a50-105">DESCRIPTION</span></span>
<span data-ttu-id="f4a50-106">Das Cmdlet " **Get-AzureRmDtlAutoStartPolicy** " Ruft die Richtlinie für den automatischen Start einer Übungseinheit ab, die virtuelle Lab-Computer für den automatischen Start plant.</span><span class="sxs-lookup"><span data-stu-id="f4a50-106">The **Get-AzureRmDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="f4a50-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie sowie die Tage der Woche und Uhrzeit zurück, die Sie festgelegt haben, damit Lab-virtuelle Computer für den automatischen Start geplant werden können.</span><span class="sxs-lookup"><span data-stu-id="f4a50-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="f4a50-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f4a50-108">EXAMPLES</span></span>

## <span data-ttu-id="f4a50-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4a50-109">PARAMETERS</span></span>

### <span data-ttu-id="f4a50-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a50-110">-DefaultProfile</span></span>
<span data-ttu-id="f4a50-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f4a50-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4a50-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="f4a50-112">-LabName</span></span>
<span data-ttu-id="f4a50-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für den automatischen Start erhält.</span><span class="sxs-lookup"><span data-stu-id="f4a50-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="f4a50-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a50-114">-ResourceGroupName</span></span>
<span data-ttu-id="f4a50-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="f4a50-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="f4a50-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a50-116">CommonParameters</span></span>
<span data-ttu-id="f4a50-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a50-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a50-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a50-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a50-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f4a50-119">INPUTS</span></span>

### <span data-ttu-id="f4a50-120">Keine</span><span class="sxs-lookup"><span data-stu-id="f4a50-120">None</span></span>
<span data-ttu-id="f4a50-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="f4a50-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4a50-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f4a50-122">OUTPUTS</span></span>

### <span data-ttu-id="f4a50-123">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="f4a50-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="f4a50-124">Dieses Cmdlet gibt den Zeitplan zurück, der angibt, wann die virtuellen Computer der Übungseinheit gestartet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f4a50-124">This cmdlet returns the schedule that specifies when the lab's virtual machines must be started.</span></span>

## <span data-ttu-id="f4a50-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="f4a50-125">NOTES</span></span>

## <span data-ttu-id="f4a50-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f4a50-126">RELATED LINKS</span></span>

[<span data-ttu-id="f4a50-127">Satz-AzureRmDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="f4a50-127">Set-AzureRmDtlAutoStartPolicy</span></span>](./Set-AzureRmDtlAutoStartPolicy.md)


