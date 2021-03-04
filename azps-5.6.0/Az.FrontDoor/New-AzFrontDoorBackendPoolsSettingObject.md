---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: c61c39bc95ae3521d7b0b573c43e303749999cbd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928160"
---
# <span data-ttu-id="07f33-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="07f33-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="07f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f33-102">SYNOPSIS</span></span>
<span data-ttu-id="07f33-103">Erstellen Sie ein PSBackendPoolsSetting-Objekt für die Erstellung von Vordertüren.</span><span class="sxs-lookup"><span data-stu-id="07f33-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="07f33-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07f33-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07f33-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07f33-105">DESCRIPTION</span></span>
<span data-ttu-id="07f33-106">Das **Cmdlet New-AzFrontDoorBackendpoolsSettingObject** erstellt ein neues PSBackendPoolsSettings-Objekt für die Erstellung von Front Door.</span><span class="sxs-lookup"><span data-stu-id="07f33-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="07f33-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07f33-107">EXAMPLES</span></span>

### <span data-ttu-id="07f33-108">Beispiel 1: Erstellen eines BackendPoolsSettings-Objekts mit Standardwerten</span><span class="sxs-lookup"><span data-stu-id="07f33-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="07f33-109">Beispiel 2: Erstellen eines BackendPoolsSettings-Objekts mit vom Benutzer angegebenen Werten</span><span class="sxs-lookup"><span data-stu-id="07f33-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="07f33-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="07f33-110">PARAMETERS</span></span>

### <span data-ttu-id="07f33-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f33-111">-DefaultProfile</span></span>
<span data-ttu-id="07f33-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07f33-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f33-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="07f33-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="07f33-114">Ob die Zertifikatnamensprüfung für HTTPS-Anforderungen an alle Back-End-Pools erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="07f33-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="07f33-115">Keine Auswirkung auf Nicht-HTTPS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="07f33-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="07f33-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="07f33-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="07f33-117">Senden und Empfangen von Timeouts bei der Weiterleitungsanforderung an das Back-End.</span><span class="sxs-lookup"><span data-stu-id="07f33-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="07f33-118">Wenn das Timeout erreicht ist, schlägt die Anforderung fehl und gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="07f33-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="07f33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f33-119">CommonParameters</span></span>
<span data-ttu-id="07f33-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f33-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07f33-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f33-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07f33-122">INPUTS</span></span>

### <span data-ttu-id="07f33-123">Keine</span><span class="sxs-lookup"><span data-stu-id="07f33-123">None</span></span>

## <span data-ttu-id="07f33-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07f33-124">OUTPUTS</span></span>

### <span data-ttu-id="07f33-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="07f33-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="07f33-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="07f33-126">NOTES</span></span>

## <span data-ttu-id="07f33-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="07f33-127">RELATED LINKS</span></span>
