---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: 850db31354ebe4a717a5064c7fed56dc94bf1f0d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845495"
---
# <span data-ttu-id="0a01e-101">New-AzFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="0a01e-101">New-AzFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="0a01e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a01e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a01e-103">Erstellen eines PSHealthProbeSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="0a01e-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0a01e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a01e-104">SYNTAX</span></span>

```
New-AzFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-HealthProbeMethod <String>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a01e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a01e-105">DESCRIPTION</span></span>
<span data-ttu-id="0a01e-106">Erstellen eines PSHealthProbeSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="0a01e-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0a01e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a01e-107">EXAMPLES</span></span>

### <span data-ttu-id="0a01e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0a01e-108">Example 1</span></span>
```powershell
PS C:\>  New-AzFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
HealthProbeMethod : Head
EnabledState      : Enabled
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="0a01e-109">Hinweis: bei der HealthProbeMethod-Einstellung wird die Groß-/Kleinschreibung nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="0a01e-109">Note: HealthProbeMethod setting is not case sensitive.</span></span>

<span data-ttu-id="0a01e-110">Erstellen eines PSHealthProbeSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="0a01e-110">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="0a01e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a01e-111">PARAMETERS</span></span>

### <span data-ttu-id="0a01e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a01e-112">-DefaultProfile</span></span>
<span data-ttu-id="0a01e-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a01e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a01e-114">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="0a01e-114">-EnabledState</span></span>
<span data-ttu-id="0a01e-115">Gibt an, ob Integritäts Prüfpunkte für die unter backendPools definierten Backends aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0a01e-115">Whether to enable health probes to be made against backends defined under backendPools.</span></span> <span data-ttu-id="0a01e-116">Integritätsprüfungen können nur deaktiviert werden, wenn ein einzelnes, aktiviertes Back-End im Single-fähigen Back-End-Pool vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0a01e-116">Health probes can only be disabled if there is a single enabled backend in single enabled backend pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a01e-117">-HealthProbeMethod</span><span class="sxs-lookup"><span data-stu-id="0a01e-117">-HealthProbeMethod</span></span>
<span data-ttu-id="0a01e-118">Konfiguriert, welche HTTP-Methode verwendet wird, um die unter backendPools definierten Backends zu sondieren.</span><span class="sxs-lookup"><span data-stu-id="0a01e-118">Configures which HTTP method to use to probe the backends defined under backendPools.</span></span>

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

### <span data-ttu-id="0a01e-119">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0a01e-119">-IntervalInSeconds</span></span>
<span data-ttu-id="0a01e-120">Die Anzahl von Sekunden zwischen Integritätsprüfungen.</span><span class="sxs-lookup"><span data-stu-id="0a01e-120">The number of seconds between health probes.</span></span>
<span data-ttu-id="0a01e-121">Der Standardwert ist 30.</span><span class="sxs-lookup"><span data-stu-id="0a01e-121">Default value is 30</span></span>

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

### <span data-ttu-id="0a01e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0a01e-122">-Name</span></span>
<span data-ttu-id="0a01e-123">Name für Integritäts Prüf Punkt Einstellung.</span><span class="sxs-lookup"><span data-stu-id="0a01e-123">Health probe setting name.</span></span>

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

### <span data-ttu-id="0a01e-124">-Path</span><span class="sxs-lookup"><span data-stu-id="0a01e-124">-Path</span></span>
<span data-ttu-id="0a01e-125">Der für den Integritäts Prüf Punkt zu verwendende Pfad.</span><span class="sxs-lookup"><span data-stu-id="0a01e-125">The path to use for the health probe.</span></span>
<span data-ttu-id="0a01e-126">Standard ist/</span><span class="sxs-lookup"><span data-stu-id="0a01e-126">Default is /</span></span>

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

### <span data-ttu-id="0a01e-127">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="0a01e-127">-Protocol</span></span>
<span data-ttu-id="0a01e-128">Für diesen Prüfpunkt zu verwendender Protokollschema Standardwert ist http</span><span class="sxs-lookup"><span data-stu-id="0a01e-128">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="0a01e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a01e-129">CommonParameters</span></span>
<span data-ttu-id="0a01e-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a01e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a01e-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a01e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a01e-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a01e-132">INPUTS</span></span>

### <span data-ttu-id="0a01e-133">Keine</span><span class="sxs-lookup"><span data-stu-id="0a01e-133">None</span></span>
## <span data-ttu-id="0a01e-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a01e-134">OUTPUTS</span></span>

### <span data-ttu-id="0a01e-135">Microsoft. Azure. Commands. Haustür. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="0a01e-135">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>
## <span data-ttu-id="0a01e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a01e-136">NOTES</span></span>

## <span data-ttu-id="0a01e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a01e-137">RELATED LINKS</span></span>

<span data-ttu-id="0a01e-138">[Neu – AzFrontDoor](./New-AzFrontDoor.md) 
 [Satz-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="0a01e-138">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
