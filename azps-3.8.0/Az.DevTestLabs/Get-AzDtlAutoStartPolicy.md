---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 9FD4DB8C-B242-4F9A-92E5-0B3EDED00521
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlAutoStartPolicy.md
ms.openlocfilehash: 8b2269b46a120d34e696b2ee160aabceb0cba66c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997062"
---
# <span data-ttu-id="ca9fc-101">Get-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="ca9fc-101">Get-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="ca9fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca9fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ca9fc-103">Ruft die Richtlinie für den automatischen Start einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-103">Gets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="ca9fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca9fc-104">SYNTAX</span></span>

```
Get-AzDtlAutoStartPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca9fc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca9fc-105">DESCRIPTION</span></span>
<span data-ttu-id="ca9fc-106">Das Cmdlet " **Get-AzDtlAutoStartPolicy** " Ruft die Richtlinie für den automatischen Start einer Übungseinheit ab, die virtuelle Lab-Computer für den automatischen Start plant.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-106">The **Get-AzDtlAutoStartPolicy** cmdlet gets the auto start policy of a lab which schedules lab virtual machines for automatic start.</span></span>
<span data-ttu-id="ca9fc-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie sowie die Tage der Woche und Uhrzeit zurück, die Sie festgelegt haben, damit Lab-virtuelle Computer für den automatischen Start geplant werden können.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-107">The cmdlet returns the enabled or disabled status of the policy and the days of the week and time of day that you have set to allow lab virtual machines to be scheduled for automatic start.</span></span>

## <span data-ttu-id="ca9fc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca9fc-108">EXAMPLES</span></span>

## <span data-ttu-id="ca9fc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca9fc-109">PARAMETERS</span></span>

### <span data-ttu-id="ca9fc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca9fc-110">-DefaultProfile</span></span>
<span data-ttu-id="ca9fc-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ca9fc-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca9fc-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="ca9fc-112">-LabName</span></span>
<span data-ttu-id="ca9fc-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die Richtlinie für den automatischen Start erhält.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-113">Specifies the name of the lab for which this cmdlet gets the auto start policy.</span></span>

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

### <span data-ttu-id="ca9fc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca9fc-114">-ResourceGroupName</span></span>
<span data-ttu-id="ca9fc-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="ca9fc-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca9fc-116">CommonParameters</span></span>
<span data-ttu-id="ca9fc-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca9fc-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca9fc-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca9fc-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca9fc-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca9fc-119">INPUTS</span></span>

### <span data-ttu-id="ca9fc-120">System. String</span><span class="sxs-lookup"><span data-stu-id="ca9fc-120">System.String</span></span>

## <span data-ttu-id="ca9fc-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca9fc-121">OUTPUTS</span></span>

### <span data-ttu-id="ca9fc-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSSchedule</span><span class="sxs-lookup"><span data-stu-id="ca9fc-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="ca9fc-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca9fc-123">NOTES</span></span>

## <span data-ttu-id="ca9fc-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca9fc-124">RELATED LINKS</span></span>

[<span data-ttu-id="ca9fc-125">Satz-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="ca9fc-125">Set-AzDtlAutoStartPolicy</span></span>](./Set-AzDtlAutoStartPolicy.md)


