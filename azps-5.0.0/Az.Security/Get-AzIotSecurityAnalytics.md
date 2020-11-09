---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzIotSecurityAnalytics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzIotSecurityAnalytics.md
ms.openlocfilehash: 56827f5a461239ceae756591b82ff687cb50053c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300940"
---
# <span data-ttu-id="69bc3-101">Get-AzIotSecurityAnalytics</span><span class="sxs-lookup"><span data-stu-id="69bc3-101">Get-AzIotSecurityAnalytics</span></span>

## <span data-ttu-id="69bc3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="69bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="69bc3-103">Abrufen von Sicherheitsanalysen</span><span class="sxs-lookup"><span data-stu-id="69bc3-103">Get IoT security analytics</span></span>

## <span data-ttu-id="69bc3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="69bc3-104">SYNTAX</span></span>

```
Get-AzIotSecurityAnalytics -ResourceGroupName <String> -SolutionName <String> [-Default]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69bc3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69bc3-105">DESCRIPTION</span></span>
<span data-ttu-id="69bc3-106">Das Get-AzIotSecurityAnalytics-Cmdlet gibt eine Reihe von Sicherheitsanalysen einer bestimmten viel Sicherheitslösung zurück.</span><span class="sxs-lookup"><span data-stu-id="69bc3-106">The Get-AzIotSecurityAnalytics cmdlet returns a set of security analytics of a specific iot security solution</span></span>

## <span data-ttu-id="69bc3-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69bc3-107">EXAMPLES</span></span>

### <span data-ttu-id="69bc3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="69bc3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzIotSecurityAnalytics -ResourceGroupName "MyResourceGroup" -SolutionName "MySolution" -Default

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolution/analyticsModels/default"
Name: "default"
Type: "Microsoft.Security/IoTSecuritySolutionAnalyticsModel"
Metrics: {
            High": 5
            Medium: 200
            Low: 102
          }
UnhealthyDeviceCount: 1200
DevicesMetrics: [
            {
              Date: "2019-02-01T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 15
                Low: 70
              }
            }
            {
              Date: "2019-02-02T00:00:00Z"
              DevicesMetrics: {
                High: 3
                Medium: 45
                Low: 65
              }
            }
          ]
TopAlertedDevices: [
            {
              DeviceId: "id1"
              AlertsCount: 200
            }
            {
              DeviceId": "id2"
              AlertsCount": 170
            }
            {
              DeviceId": "id3"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceAlerts: [
            {
              AlertDisplayName: "Custom Alert - number of device to cloud messages in AMQP protocol is not in the allowed range"
              ReportedSeverity: "Low"
              AlertsCount: 200
            }
            {
              AlertDisplayName: "Custom Alert - execution of a process that is not allowed"
              ReportedSeverity: "Medium"
              AlertsCount: 170
            }
            {
              AlertDisplayName": "Successful Bruteforce"
              ReportedSeverity": "Low"
              AlertsCount": 150
            }
          ]
MostPrevalentDeviceRecommendations: [
            {
              RecommendationDisplayName: "Install the Azure Security of Things Agent"
              ReportedSeverity: "Low"
              DevicesCount: 200
            }
            {
              RecommendationDisplayName: "High level permissions configured in Edge model twin for Edge module"
              ReportedSeverity: "Low"
              DevicesCount: 170
            }
            {
              RrecommendationDisplayName: "Same Authentication Credentials used by multiple devices"
              ReportedSeverity: "Medium"
              DevicesCount: 150
            }
          ]
        }
      }
```

<span data-ttu-id="69bc3-109">Holen Sie sich die deafult viel Security Analytics for Security-Lösung "MySolution" in der dasselbe Benuteroberflächenmodell-Gruppe "myresourcegroup"</span><span class="sxs-lookup"><span data-stu-id="69bc3-109">Get the deafult IoT Security Analytics for Security Solution "MySolution" in reasource group "MyResourceGroup"</span></span>

## <span data-ttu-id="69bc3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="69bc3-110">PARAMETERS</span></span>

### <span data-ttu-id="69bc3-111">– Standard</span><span class="sxs-lookup"><span data-stu-id="69bc3-111">-Default</span></span>
<span data-ttu-id="69bc3-112">Wenn vorhanden, rufen Sie den standardmäßigen Analyse Satz ab, und rufen Sie andernfalls die Liste aller Analyse Sätze ab.</span><span class="sxs-lookup"><span data-stu-id="69bc3-112">If present, get the default analytics set, otherwise, get the list of all analytics sets.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69bc3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69bc3-113">-DefaultProfile</span></span>
<span data-ttu-id="69bc3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="69bc3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69bc3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69bc3-115">-ResourceGroupName</span></span>
<span data-ttu-id="69bc3-116">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="69bc3-116">Resource group name.</span></span>

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

### <span data-ttu-id="69bc3-117">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="69bc3-117">-SolutionName</span></span>
<span data-ttu-id="69bc3-118">Projektmappenname</span><span class="sxs-lookup"><span data-stu-id="69bc3-118">Solution name</span></span>

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

### <span data-ttu-id="69bc3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69bc3-119">CommonParameters</span></span>
<span data-ttu-id="69bc3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69bc3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69bc3-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69bc3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69bc3-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="69bc3-122">INPUTS</span></span>

### <span data-ttu-id="69bc3-123">Keine</span><span class="sxs-lookup"><span data-stu-id="69bc3-123">None</span></span>

## <span data-ttu-id="69bc3-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="69bc3-124">OUTPUTS</span></span>

### <span data-ttu-id="69bc3-125">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIotSecuritySolutionAnalytics</span><span class="sxs-lookup"><span data-stu-id="69bc3-125">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIotSecuritySolutionAnalytics</span></span>

## <span data-ttu-id="69bc3-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="69bc3-126">NOTES</span></span>

## <span data-ttu-id="69bc3-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="69bc3-127">RELATED LINKS</span></span>
