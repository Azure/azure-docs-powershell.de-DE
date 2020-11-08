---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995906"
---
# <span data-ttu-id="ca805-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="ca805-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="ca805-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ca805-102">SYNOPSIS</span></span>
<span data-ttu-id="ca805-103">Ruft Informationen zum Warnungsverlauf ab</span><span class="sxs-lookup"><span data-stu-id="ca805-103">Gets Alert History information</span></span>

## <span data-ttu-id="ca805-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca805-104">SYNTAX</span></span>

### <span data-ttu-id="ca805-105">ByAlertId (Standard)</span><span class="sxs-lookup"><span data-stu-id="ca805-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca805-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ca805-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca805-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca805-107">DESCRIPTION</span></span>
<span data-ttu-id="ca805-108">Das Cmdlet " **Get-AzAlertObjectHistory** " Ruft den Warnungsverlauf ab.</span><span class="sxs-lookup"><span data-stu-id="ca805-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="ca805-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ca805-109">EXAMPLES</span></span>

### <span data-ttu-id="ca805-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca805-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="ca805-111">Ruft Details des Warnungs Verlaufs ab.</span><span class="sxs-lookup"><span data-stu-id="ca805-111">Gets alert history details.</span></span> 

## <span data-ttu-id="ca805-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca805-112">PARAMETERS</span></span>

### <span data-ttu-id="ca805-113">-Warnungs-Nr.</span><span class="sxs-lookup"><span data-stu-id="ca805-113">-AlertId</span></span>
<span data-ttu-id="ca805-114">Eindeutiger Bezeichner der Benachrichtigungs-ID.</span><span class="sxs-lookup"><span data-stu-id="ca805-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca805-115">-DefaultProfile</span></span>
<span data-ttu-id="ca805-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ca805-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca805-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ca805-117">-InputObject</span></span>
<span data-ttu-id="ca805-118">Eingabeobjekt aus Pipeline.</span><span class="sxs-lookup"><span data-stu-id="ca805-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca805-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca805-119">CommonParameters</span></span>
<span data-ttu-id="ca805-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca805-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca805-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca805-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca805-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ca805-122">INPUTS</span></span>

### <span data-ttu-id="ca805-123">Keine</span><span class="sxs-lookup"><span data-stu-id="ca805-123">None</span></span>

## <span data-ttu-id="ca805-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ca805-124">OUTPUTS</span></span>

### <span data-ttu-id="ca805-125">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="ca805-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="ca805-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="ca805-126">NOTES</span></span>

## <span data-ttu-id="ca805-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ca805-127">RELATED LINKS</span></span>
