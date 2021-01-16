---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306211"
---
# <span data-ttu-id="328fe-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="328fe-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="328fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="328fe-102">SYNOPSIS</span></span>
<span data-ttu-id="328fe-103">Ruft einen Wiederherstellungsplan oder alle Wiederherstellungspläne im Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="328fe-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="328fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="328fe-104">SYNTAX</span></span>

### <span data-ttu-id="328fe-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="328fe-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="328fe-106">ByName</span><span class="sxs-lookup"><span data-stu-id="328fe-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="328fe-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="328fe-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="328fe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="328fe-108">DESCRIPTION</span></span>
<span data-ttu-id="328fe-109">Das **Cmdlet "Get-AzRecoveryServicesAsrRecoveryPlan"** ruft die Details des angegebenen Wiederherstellungsplans oder aller Wiederherstellungspläne im Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="328fe-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="328fe-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="328fe-110">EXAMPLES</span></span>

### <span data-ttu-id="328fe-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="328fe-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="328fe-112">Ruft den Wiederherstellungsplan mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="328fe-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="328fe-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="328fe-113">PARAMETERS</span></span>

### <span data-ttu-id="328fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="328fe-114">-DefaultProfile</span></span>
<span data-ttu-id="328fe-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="328fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="328fe-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="328fe-116">-FriendlyName</span></span>
<span data-ttu-id="328fe-117">Gibt den Anzeigenamen des wiederherstellungsplans an, den Sie erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="328fe-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fe-118">-Name</span><span class="sxs-lookup"><span data-stu-id="328fe-118">-Name</span></span>
<span data-ttu-id="328fe-119">Gibt den Namen des wiederherstellungsplans an, den Sie erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="328fe-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fe-120">-Path</span><span class="sxs-lookup"><span data-stu-id="328fe-120">-Path</span></span>
<span data-ttu-id="328fe-121">Gibt den Dateipfad an, unter dem dieses Cmdlet die json-Definition des Wiederherstellungsplans speichert.</span><span class="sxs-lookup"><span data-stu-id="328fe-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="328fe-122">Die json-Definition kann bearbeitet werden, um den Wiederherstellungsplan zu ändern, und verwendet werden, um den Wiederherstellungsplan über das Cmdlet Update-AzRecoveryServicesASRRecoveryPlan aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="328fe-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="328fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="328fe-123">CommonParameters</span></span>
<span data-ttu-id="328fe-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="328fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="328fe-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="328fe-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="328fe-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="328fe-126">INPUTS</span></span>

### <span data-ttu-id="328fe-127">Keine</span><span class="sxs-lookup"><span data-stu-id="328fe-127">None</span></span>

## <span data-ttu-id="328fe-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="328fe-128">OUTPUTS</span></span>

### <span data-ttu-id="328fe-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="328fe-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="328fe-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="328fe-130">NOTES</span></span>

## <span data-ttu-id="328fe-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="328fe-131">RELATED LINKS</span></span>

[<span data-ttu-id="328fe-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="328fe-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="328fe-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="328fe-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="328fe-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="328fe-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
