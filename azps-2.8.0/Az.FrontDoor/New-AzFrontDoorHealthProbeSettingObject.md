---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 60eaa3b5482d6d1c13236560f797383d68d97b44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651125"
---
# <span data-ttu-id="42d5d-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="42d5d-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="42d5d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42d5d-102">SYNOPSIS</span></span>
<span data-ttu-id="42d5d-103">Erstellen eines PSHealthProbeSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="42d5d-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="42d5d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42d5d-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d5d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42d5d-105">DESCRIPTION</span></span>
<span data-ttu-id="42d5d-106">Erstellen eines PSHealthProbeSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="42d5d-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="42d5d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42d5d-107">EXAMPLES</span></span>

### <span data-ttu-id="42d5d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="42d5d-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="42d5d-109">Erstellen eines PSHealthProbeSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="42d5d-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="42d5d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="42d5d-110">PARAMETERS</span></span>

### <span data-ttu-id="42d5d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d5d-111">-DefaultProfile</span></span>
<span data-ttu-id="42d5d-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42d5d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42d5d-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="42d5d-113">-IntervalInSeconds</span></span>
<span data-ttu-id="42d5d-114">Die Anzahl von Sekunden zwischen Integritätsprüfungen.</span><span class="sxs-lookup"><span data-stu-id="42d5d-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="42d5d-115">Der Standardwert ist 30.</span><span class="sxs-lookup"><span data-stu-id="42d5d-115">Default value is 30</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="42d5d-116">-Name</span></span>
<span data-ttu-id="42d5d-117">Name für Integritäts Prüf Punkt Einstellung.</span><span class="sxs-lookup"><span data-stu-id="42d5d-117">health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-118">-Path</span><span class="sxs-lookup"><span data-stu-id="42d5d-118">-Path</span></span>
<span data-ttu-id="42d5d-119">Der für den Integritäts Prüf Punkt zu verwendende Pfad.</span><span class="sxs-lookup"><span data-stu-id="42d5d-119">The path to use for the health probe.</span></span>
<span data-ttu-id="42d5d-120">Standard ist/</span><span class="sxs-lookup"><span data-stu-id="42d5d-120">Default is /</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-121">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="42d5d-121">-Protocol</span></span>
<span data-ttu-id="42d5d-122">Für diesen Prüfpunkt zu verwendender Protokollschema Standardwert ist http</span><span class="sxs-lookup"><span data-stu-id="42d5d-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocol
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42d5d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d5d-123">CommonParameters</span></span>
<span data-ttu-id="42d5d-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d5d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d5d-125">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42d5d-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d5d-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42d5d-126">INPUTS</span></span>

### <span data-ttu-id="42d5d-127">Keine</span><span class="sxs-lookup"><span data-stu-id="42d5d-127">None</span></span>

## <span data-ttu-id="42d5d-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42d5d-128">OUTPUTS</span></span>

### <span data-ttu-id="42d5d-129">Microsoft. Azure. Commands. Haustür. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="42d5d-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="42d5d-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="42d5d-130">NOTES</span></span>

## <span data-ttu-id="42d5d-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42d5d-131">RELATED LINKS</span></span>

<span data-ttu-id="42d5d-132">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="42d5d-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
