---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469803"
---
# <span data-ttu-id="715e5-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="715e5-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="715e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="715e5-102">SYNOPSIS</span></span>
<span data-ttu-id="715e5-103">Erstellen Sie ein "PSBackendPoolsSetting"-Objekt für die Erstellung von Front Door.</span><span class="sxs-lookup"><span data-stu-id="715e5-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="715e5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="715e5-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="715e5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="715e5-105">DESCRIPTION</span></span>
<span data-ttu-id="715e5-106">Das **Cmdlet "New-AzFrontD selbstBackendpoolsSettingObject"** erstellt ein neues PSBackendPoolsSettings-Objekt für die Erstellung von Front Door.</span><span class="sxs-lookup"><span data-stu-id="715e5-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="715e5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="715e5-107">EXAMPLES</span></span>

### <span data-ttu-id="715e5-108">Beispiel 1: Erstellen eines Back-EndPoolsSettings-Objekts mit Standardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="715e5-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="715e5-109">Beispiel 2: Erstellen eines Back-EndPoolsSettings-Objekts mit vom Benutzer angegebenen Werten</span><span class="sxs-lookup"><span data-stu-id="715e5-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="715e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="715e5-110">PARAMETERS</span></span>

### <span data-ttu-id="715e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715e5-111">-DefaultProfile</span></span>
<span data-ttu-id="715e5-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="715e5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="715e5-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="715e5-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="715e5-114">Gibt an, ob die Überprüfung des Zertifikatnamens für https-Anforderungen an alle Back-End-Pools erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="715e5-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="715e5-115">Keine Auswirkung auf Nicht-HTTPS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="715e5-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="715e5-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="715e5-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="715e5-117">Timeout für Senden und Empfangen einer Weiterleitungsanforderung an das Back-End.</span><span class="sxs-lookup"><span data-stu-id="715e5-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="715e5-118">Wenn das Timeout erreicht ist, schlägt die Anforderung fehl und wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="715e5-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="715e5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715e5-119">CommonParameters</span></span>
<span data-ttu-id="715e5-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715e5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715e5-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="715e5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715e5-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="715e5-122">INPUTS</span></span>

### <span data-ttu-id="715e5-123">Keine</span><span class="sxs-lookup"><span data-stu-id="715e5-123">None</span></span>

## <span data-ttu-id="715e5-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="715e5-124">OUTPUTS</span></span>

### <span data-ttu-id="715e5-125">Microsoft.Azure.Commands.FrontD selbst.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="715e5-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="715e5-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="715e5-126">NOTES</span></span>

## <span data-ttu-id="715e5-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="715e5-127">RELATED LINKS</span></span>
