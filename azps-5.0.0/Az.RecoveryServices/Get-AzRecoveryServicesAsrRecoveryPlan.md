---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 4873c30caf0f1b59bf9be848f44c6e1358649b69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176773"
---
# <span data-ttu-id="9bf60-101">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9bf60-101">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="9bf60-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9bf60-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf60-103">Ruft einen Wiederherstellungsplan oder alle Wiederherstellungspläne im Speicher für Wiederherstellungsdienste ab</span><span class="sxs-lookup"><span data-stu-id="9bf60-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

## <span data-ttu-id="9bf60-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bf60-104">SYNTAX</span></span>

### <span data-ttu-id="9bf60-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="9bf60-105">Default (Default)</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bf60-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9bf60-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9bf60-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9bf60-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf60-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bf60-108">DESCRIPTION</span></span>
<span data-ttu-id="9bf60-109">Mit dem Cmdlet **Get-AzRecoveryServicesAsrRecoveryPlan werden** die Details des angegebenen Wiederherstellungsplans oder aller Wiederherstellungspläne im Vault für Wiederherstellungsdienste abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9bf60-109">The **Get-AzRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="9bf60-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bf60-110">EXAMPLES</span></span>

### <span data-ttu-id="9bf60-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9bf60-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="9bf60-112">Ruft den Wiederherstellungsplan mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="9bf60-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="9bf60-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bf60-113">PARAMETERS</span></span>

### <span data-ttu-id="9bf60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf60-114">-DefaultProfile</span></span>
<span data-ttu-id="9bf60-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9bf60-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9bf60-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9bf60-116">-FriendlyName</span></span>
<span data-ttu-id="9bf60-117">Gibt den Anzeigenamen des Wiederherstellungsplans an, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bf60-117">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="9bf60-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9bf60-118">-Name</span></span>
<span data-ttu-id="9bf60-119">Gibt den Namen des abzurufenden Wiederherstellungsplans an.</span><span class="sxs-lookup"><span data-stu-id="9bf60-119">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="9bf60-120">-Path</span><span class="sxs-lookup"><span data-stu-id="9bf60-120">-Path</span></span>
<span data-ttu-id="9bf60-121">Gibt den Dateipfad an, zu dem dieses Cmdlet die JSON-Definition für den Wiederherstellungsplan speichert.</span><span class="sxs-lookup"><span data-stu-id="9bf60-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="9bf60-122">Die JSON-Definition kann bearbeitet werden, um den Wiederherstellungsplan zu ändern und den Wiederherstellungsplan über das Update-AzRecoveryServicesASRRecoveryPlan-Cmdlet zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9bf60-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="9bf60-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf60-123">CommonParameters</span></span>
<span data-ttu-id="9bf60-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf60-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf60-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bf60-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf60-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9bf60-126">INPUTS</span></span>

### <span data-ttu-id="9bf60-127">Keine</span><span class="sxs-lookup"><span data-stu-id="9bf60-127">None</span></span>

## <span data-ttu-id="9bf60-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9bf60-128">OUTPUTS</span></span>

### <span data-ttu-id="9bf60-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9bf60-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="9bf60-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9bf60-130">NOTES</span></span>

## <span data-ttu-id="9bf60-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9bf60-131">RELATED LINKS</span></span>

[<span data-ttu-id="9bf60-132">Neu – AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9bf60-132">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9bf60-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9bf60-133">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9bf60-134">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9bf60-134">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)
