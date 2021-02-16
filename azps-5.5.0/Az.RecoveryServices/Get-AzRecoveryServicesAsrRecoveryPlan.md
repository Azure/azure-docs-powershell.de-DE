---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169276"
---
# <span data-ttu-id="98ec0-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98ec0-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="98ec0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98ec0-102">SYNOPSIS</span></span>
<span data-ttu-id="98ec0-103">Ruft einen Wiederherstellungsplan oder alle Wiederherstellungspläne im Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="98ec0-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="98ec0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98ec0-104">SYNTAX</span></span>

### <span data-ttu-id="98ec0-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="98ec0-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98ec0-106">ByName</span><span class="sxs-lookup"><span data-stu-id="98ec0-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98ec0-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="98ec0-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98ec0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98ec0-108">DESCRIPTION</span></span>
<span data-ttu-id="98ec0-109">Das **Cmdlet "Get-AzRecoveryServicesAsrRecoveryPlan"** ruft die Details des angegebenen Wiederherstellungsplans oder aller Wiederherstellungspläne im Wiederherstellungsdiensttresor ab.</span><span class="sxs-lookup"><span data-stu-id="98ec0-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="98ec0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98ec0-110">EXAMPLES</span></span>

### <span data-ttu-id="98ec0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98ec0-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="98ec0-112">Ruft den Wiederherstellungsplan mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="98ec0-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="98ec0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98ec0-113">PARAMETERS</span></span>

### <span data-ttu-id="98ec0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ec0-114">-DefaultProfile</span></span>
<span data-ttu-id="98ec0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98ec0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="98ec0-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="98ec0-116">-FriendlyName</span></span>
<span data-ttu-id="98ec0-117">Gibt den Anzeigenamen des wiederherstellungsplans an, den Sie erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="98ec0-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="98ec0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="98ec0-118">-Name</span></span>
<span data-ttu-id="98ec0-119">Gibt den Namen des wiederherstellungsplans an, den Sie erhalten sollen.</span><span class="sxs-lookup"><span data-stu-id="98ec0-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="98ec0-120">-Path</span><span class="sxs-lookup"><span data-stu-id="98ec0-120">-Path</span></span>
<span data-ttu-id="98ec0-121">Gibt den Dateipfad an, unter dem dieses Cmdlet die json-Definition des Wiederherstellungsplans speichert.</span><span class="sxs-lookup"><span data-stu-id="98ec0-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="98ec0-122">Die json-Definition kann bearbeitet werden, um den Wiederherstellungsplan zu ändern, und verwendet werden, um den Wiederherstellungsplan über das Cmdlet Update-AzRecoveryServicesASRRecoveryPlan aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="98ec0-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="98ec0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ec0-123">CommonParameters</span></span>
<span data-ttu-id="98ec0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98ec0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ec0-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98ec0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ec0-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98ec0-126">INPUTS</span></span>

### <span data-ttu-id="98ec0-127">Keine</span><span class="sxs-lookup"><span data-stu-id="98ec0-127">None</span></span>

## <span data-ttu-id="98ec0-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98ec0-128">OUTPUTS</span></span>

### <span data-ttu-id="98ec0-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98ec0-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="98ec0-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="98ec0-130">NOTES</span></span>

## <span data-ttu-id="98ec0-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="98ec0-131">RELATED LINKS</span></span>

[<span data-ttu-id="98ec0-132">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98ec0-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="98ec0-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98ec0-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="98ec0-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="98ec0-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
