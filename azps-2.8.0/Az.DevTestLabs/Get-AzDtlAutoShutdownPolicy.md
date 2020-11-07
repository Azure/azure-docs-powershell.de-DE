---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 52DD0511-915F-4144-B47F-E4B7AF403AA5
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b34a60fa2b85f18a5bee10e0e1f66a4ab102c7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651319"
---
# <span data-ttu-id="587f0-101">Get-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="587f0-101">Get-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="587f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="587f0-102">SYNOPSIS</span></span>
<span data-ttu-id="587f0-103">Ruft die Richtlinie für das automatische Herunterfahren einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="587f0-103">Gets the auto shutdown policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="587f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="587f0-104">SYNTAX</span></span>

```
Get-AzDtlAutoShutdownPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="587f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="587f0-105">DESCRIPTION</span></span>
<span data-ttu-id="587f0-106">Das Cmdlet " **Get-AzDtlAutoShutdownPolicy** " Ruft die Richtlinie für das automatische Herunterfahren einer Übungseinheit ab, mit der Sie alle virtuellen Computer in einer Übungseinheit automatisch zu einer bestimmten Tageszeit Herunterfahren können.</span><span class="sxs-lookup"><span data-stu-id="587f0-106">The **Get-AzDtlAutoShutdownPolicy** cmdlet gets the auto shutdown policy of a lab, which allows you to automatically shut down all the virtual machines in a lab at a specified time of the day.</span></span>
<span data-ttu-id="587f0-107">Das Cmdlet gibt zurück, ob der Status der Richtlinie aktiviert ist, und die Tageszeit, die Sie festgelegt haben, um die virtuellen Lab-Computer automatisch herunterzufahren.</span><span class="sxs-lookup"><span data-stu-id="587f0-107">The cmdlet returns whether the status of the policy is enabled, and the time of day that you have set to automatically shut down the lab virtual machines.</span></span>

## <span data-ttu-id="587f0-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="587f0-108">EXAMPLES</span></span>

## <span data-ttu-id="587f0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="587f0-109">PARAMETERS</span></span>

### <span data-ttu-id="587f0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587f0-110">-DefaultProfile</span></span>
<span data-ttu-id="587f0-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="587f0-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="587f0-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="587f0-112">-LabName</span></span>
<span data-ttu-id="587f0-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für das automatische Herunterfahren erhält.</span><span class="sxs-lookup"><span data-stu-id="587f0-113">Specifies the name of the lab for which this cmdlet gets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="587f0-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="587f0-114">-ResourceGroupName</span></span>
<span data-ttu-id="587f0-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="587f0-115">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="587f0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587f0-116">CommonParameters</span></span>
<span data-ttu-id="587f0-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="587f0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587f0-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="587f0-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587f0-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="587f0-119">INPUTS</span></span>

### <span data-ttu-id="587f0-120">System. String</span><span class="sxs-lookup"><span data-stu-id="587f0-120">System.String</span></span>

## <span data-ttu-id="587f0-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="587f0-121">OUTPUTS</span></span>

### <span data-ttu-id="587f0-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="587f0-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="587f0-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="587f0-123">NOTES</span></span>

## <span data-ttu-id="587f0-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="587f0-124">RELATED LINKS</span></span>

[<span data-ttu-id="587f0-125">Satz-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="587f0-125">Set-AzDtlAutoShutdownPolicy</span></span>](./Set-AzDtlAutoShutdownPolicy.md)


