---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendpoolssettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendPoolsSettingObject.md
ms.openlocfilehash: 9a5da13880b09b3527f1f515ca9ace9cb2442917
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177629"
---
# <span data-ttu-id="315f4-101">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="315f4-101">New-AzFrontDoorBackendPoolsSettingObject</span></span>

## <span data-ttu-id="315f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="315f4-102">SYNOPSIS</span></span>
<span data-ttu-id="315f4-103">Erstellen Sie ein PSBackendPoolsSetting-Objekt für die Haustür Erstellung.</span><span class="sxs-lookup"><span data-stu-id="315f4-103">Create a PSBackendPoolsSetting object for Front Door creation.</span></span>

## <span data-ttu-id="315f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="315f4-104">SYNTAX</span></span>

```
New-AzFrontDoorBackendPoolsSettingObject [-EnforceCertificateNameCheck <PSEnabledState>]
 [-SendRecvTimeoutInSeconds <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="315f4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="315f4-105">DESCRIPTION</span></span>
<span data-ttu-id="315f4-106">Das Cmdlet **New-AzFrontDoorBackendpoolsSettingObject** erstellt ein neues PSBackendPoolsSettings-Objekt für die Erstellung von Haustür.</span><span class="sxs-lookup"><span data-stu-id="315f4-106">The **New-AzFrontDoorBackendpoolsSettingObject** cmdlet creates a new PSBackendPoolsSettings object for Front Door creation.</span></span>

## <span data-ttu-id="315f4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="315f4-107">EXAMPLES</span></span>

### <span data-ttu-id="315f4-108">Beispiel 1: Erstellen eines BackendPoolsSettings-Objekts mit Standardeinstellungen</span><span class="sxs-lookup"><span data-stu-id="315f4-108">Example 1: Create BackendPoolsSettings object using defaults</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 30
Id                          :
Name                        :
Type                        :
```

### <span data-ttu-id="315f4-109">Beispiel 2: Erstellen eines BackendPoolsSettings-Objekts mit vom Benutzer angegebenen Werten</span><span class="sxs-lookup"><span data-stu-id="315f4-109">Example 2: Create BackendPoolsSettings object with user specified values</span></span>
```powershell
PS C:\> New-AzFrontDoorBackendpoolsSettingObject -SendRecvTimeoutInSeconds 60 -EnforceCertificateNameCheck Enabled


EnforceCertificateNameCheck : Enabled
SendRecvTimeoutInSeconds      : 60
Id                          :
Name                        :
Type                        :
```

## <span data-ttu-id="315f4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="315f4-110">PARAMETERS</span></span>

### <span data-ttu-id="315f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315f4-111">-DefaultProfile</span></span>
<span data-ttu-id="315f4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="315f4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="315f4-113">-EnforceCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="315f4-113">-EnforceCertificateNameCheck</span></span>
<span data-ttu-id="315f4-114">Ob die Zertifikatnamen Überprüfung für HTTPS-Anforderungen an alle Back-End-Pools erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="315f4-114">Whether to enforce certificate name check on HTTPS requests to all backend pools.</span></span>
<span data-ttu-id="315f4-115">Keine Auswirkungen auf nicht-HTTPS-Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="315f4-115">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="315f4-116">-SendRecvTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="315f4-116">-SendRecvTimeoutInSeconds</span></span>
<span data-ttu-id="315f4-117">Sende-und Empfangs Timeout bei der Weiterleitung der Anforderung an das Back-End.</span><span class="sxs-lookup"><span data-stu-id="315f4-117">Send and receive timeout on forwarding request to the backend.</span></span> <span data-ttu-id="315f4-118">Wenn Timeout erreicht ist, schlägt die Anforderung fehl, und es wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="315f4-118">When timeout is reached, the request fails and returns.</span></span>

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

### <span data-ttu-id="315f4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315f4-119">CommonParameters</span></span>
<span data-ttu-id="315f4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="315f4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315f4-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="315f4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315f4-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="315f4-122">INPUTS</span></span>

### <span data-ttu-id="315f4-123">Keine</span><span class="sxs-lookup"><span data-stu-id="315f4-123">None</span></span>

## <span data-ttu-id="315f4-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="315f4-124">OUTPUTS</span></span>

### <span data-ttu-id="315f4-125">Microsoft. Azure. Commands. Haustür. Models. PSBackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="315f4-125">Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting</span></span>

## <span data-ttu-id="315f4-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="315f4-126">NOTES</span></span>

## <span data-ttu-id="315f4-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="315f4-127">RELATED LINKS</span></span>
