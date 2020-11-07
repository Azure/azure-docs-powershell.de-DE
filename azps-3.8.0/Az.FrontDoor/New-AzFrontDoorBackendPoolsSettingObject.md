---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845507"
---
# <span data-ttu-id="5853e-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="5853e-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="5853e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5853e-102">SYNOPSIS</span></span>
<span data-ttu-id="5853e-103">Erstellen Sie ein PSBackendPoolsSetting-Objekt für die Haustür Erstellung.</span><span class="sxs-lookup"><span data-stu-id="5853e-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="5853e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5853e-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5853e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5853e-105">DESCRIPTION</span></span>
<span data-ttu-id="5853e-106">Das Cmdlet **New-AzFrontDoorBackendpoolsSettingObject** erstellt ein neues PSBackendPoolsSettings-Objekt für die Erstellung von Haustür.</span><span class="sxs-lookup"><span data-stu-id="5853e-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="5853e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5853e-107">EXAMPLES</span></span>

### <span data-ttu-id="5853e-108">Beispiel 1: Erstellen eines BackendPoolsSettings-Objekts mit Standardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="5853e-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="5853e-109">Beispiel 2: Erstellen eines BackendPoolsSettings-Objekts mit vom Benutzer angegebenen Werten</span><span class="sxs-lookup"><span data-stu-id="5853e-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="5853e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5853e-110">PARAMETERS</span></span>

### <span data-ttu-id="5853e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5853e-111">-DefaultProfile</span></span>
<span data-ttu-id="5853e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5853e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5853e-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="5853e-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="5853e-114">Ob die Zertifikatnamen Überprüfung für HTTPS-Anforderungen an alle Back-End-Pools erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5853e-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="5853e-115">Keine Auswirkungen auf nicht-HTTPS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="5853e-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="5853e-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="5853e-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="5853e-117">Sende-und Empfangs Timeout bei der Weiterleitung der Anforderung an das Back-End.</span><span class="sxs-lookup"><span data-stu-id="5853e-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="5853e-118">Wenn Timeout erreicht ist, schlägt die Anforderung fehl, und es wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5853e-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="5853e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5853e-119">CommonParameters</span></span>
<span data-ttu-id="5853e-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5853e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5853e-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5853e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5853e-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5853e-122">INPUTS</span></span>

### <span data-ttu-id="5853e-123">Keine</span><span class="sxs-lookup"><span data-stu-id="5853e-123">None</span></span>

## <span data-ttu-id="5853e-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5853e-124">OUTPUTS</span></span>

### <span data-ttu-id="5853e-125">Microsoft. Azure. Commands. Haustür. Models. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="5853e-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="5853e-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="5853e-126">NOTES</span></span>

## <span data-ttu-id="5853e-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5853e-127">RELATED LINKS</span></span>
