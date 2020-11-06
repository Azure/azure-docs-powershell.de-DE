---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorhealthprobesettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorHealthProbeSettingObject.md
ms.openlocfilehash: dcaf61b9001093d25f351d03e8e50da4c4ca22ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496178"
---
# <span data-ttu-id="f5b3a-101">New-AzureRmFrontDoorHealthProbeSettingObject</span><span class="sxs-lookup"><span data-stu-id="f5b3a-101">New-AzureRmFrontDoorHealthProbeSettingObject</span></span>

## <span data-ttu-id="f5b3a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b3a-103">Erstellen eines PSHealthProbeSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="f5b3a-103">Create a PSHealthProbeSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5b3a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5b3a-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorHealthProbeSettingObject -Name <String> [-Path <String>] [-Protocol <PSProtocol>]
 [-IntervalInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5b3a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5b3a-105">DESCRIPTION</span></span>
<span data-ttu-id="f5b3a-106">Erstellen eines PSHealthProbeSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="f5b3a-106">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="f5b3a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5b3a-107">EXAMPLES</span></span>

### <span data-ttu-id="f5b3a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f5b3a-108">Example 1</span></span>
```powershell
PS C:\>  New-AzureRmFrontDoorHealthProbeSettingObject -Name "healthProbeSetting1"


Path              : /
Protocol          : Http
IntervalInSeconds : 30
ResourceState     :
Id                :
Name              : healthProbeSetting1
Type              :
```

<span data-ttu-id="f5b3a-109">Erstellen eines PSHealthProbeSetting-Objekts für die Haustür Erstellung</span><span class="sxs-lookup"><span data-stu-id="f5b3a-109">Create a PSHealthProbeSetting object for Front Door creation</span></span>

## <span data-ttu-id="f5b3a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5b3a-110">PARAMETERS</span></span>

### <span data-ttu-id="f5b3a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b3a-111">-DefaultProfile</span></span>
<span data-ttu-id="f5b3a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5b3a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5b3a-113">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f5b3a-113">-IntervalInSeconds</span></span>
<span data-ttu-id="f5b3a-114">Die Anzahl von Sekunden zwischen Integritätsprüfungen.</span><span class="sxs-lookup"><span data-stu-id="f5b3a-114">The number of seconds between health probes.</span></span>
<span data-ttu-id="f5b3a-115">Der Standardwert ist 30.</span><span class="sxs-lookup"><span data-stu-id="f5b3a-115">Default value is 30</span></span>

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

### <span data-ttu-id="f5b3a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f5b3a-116">-Name</span></span>
<span data-ttu-id="f5b3a-117">Name für Integritäts Prüf Punkt Einstellung.</span><span class="sxs-lookup"><span data-stu-id="f5b3a-117">health probe setting name.</span></span>

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

### <span data-ttu-id="f5b3a-118">-Path</span><span class="sxs-lookup"><span data-stu-id="f5b3a-118">-Path</span></span>
<span data-ttu-id="f5b3a-119">Der für den Integritäts Prüf Punkt zu verwendende Pfad.</span><span class="sxs-lookup"><span data-stu-id="f5b3a-119">The path to use for the health probe.</span></span>
<span data-ttu-id="f5b3a-120">Standard ist/</span><span class="sxs-lookup"><span data-stu-id="f5b3a-120">Default is /</span></span>

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

### <span data-ttu-id="f5b3a-121">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="f5b3a-121">-Protocol</span></span>
<span data-ttu-id="f5b3a-122">Für diesen Prüfpunkt zu verwendender Protokollschema Standardwert ist http</span><span class="sxs-lookup"><span data-stu-id="f5b3a-122">Protocol scheme to use for this probe Default value is HTTP</span></span>

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

### <span data-ttu-id="f5b3a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b3a-123">CommonParameters</span></span>
<span data-ttu-id="f5b3a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5b3a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b3a-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b3a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b3a-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5b3a-126">INPUTS</span></span>

### <span data-ttu-id="f5b3a-127">Keine</span><span class="sxs-lookup"><span data-stu-id="f5b3a-127">None</span></span>

## <span data-ttu-id="f5b3a-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5b3a-128">OUTPUTS</span></span>

### <span data-ttu-id="f5b3a-129">Microsoft. Azure. Commands. Haustür. Models. PSHealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="f5b3a-129">Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting</span></span>

## <span data-ttu-id="f5b3a-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5b3a-130">NOTES</span></span>

## <span data-ttu-id="f5b3a-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5b3a-131">RELATED LINKS</span></span>

<span data-ttu-id="f5b3a-132">[Neu – AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Satz-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="f5b3a-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
