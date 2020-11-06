---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b95c3ab14d50558ef184beabcd461a59bb1a05ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481030"
---
# <span data-ttu-id="40758-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="40758-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="40758-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="40758-102">SYNOPSIS</span></span>
<span data-ttu-id="40758-103">Ruft einen Wiederherstellungsplan oder alle Wiederherstellungspläne im Speicher für Wiederherstellungsdienste ab</span><span class="sxs-lookup"><span data-stu-id="40758-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40758-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="40758-104">SYNTAX</span></span>

### <span data-ttu-id="40758-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="40758-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40758-106">ByName</span><span class="sxs-lookup"><span data-stu-id="40758-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40758-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="40758-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40758-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="40758-108">DESCRIPTION</span></span>
<span data-ttu-id="40758-109">Mit dem Cmdlet **Get-AzureRmRecoveryServicesAsrRecoveryPlan werden** die Details des angegebenen Wiederherstellungsplans oder aller Wiederherstellungspläne im Vault für Wiederherstellungsdienste abgerufen.</span><span class="sxs-lookup"><span data-stu-id="40758-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="40758-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="40758-110">EXAMPLES</span></span>

### <span data-ttu-id="40758-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="40758-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="40758-112">Ruft den Wiederherstellungsplan mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="40758-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="40758-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="40758-113">PARAMETERS</span></span>

### <span data-ttu-id="40758-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40758-114">-DefaultProfile</span></span>
<span data-ttu-id="40758-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="40758-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40758-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="40758-116">-FriendlyName</span></span>
<span data-ttu-id="40758-117">Gibt den Anzeigenamen des Wiederherstellungsplans an, der abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="40758-117">Specifies the friendly name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40758-118">-Name</span><span class="sxs-lookup"><span data-stu-id="40758-118">-Name</span></span>
<span data-ttu-id="40758-119">Gibt den Namen des abzurufenden Wiederherstellungsplans an.</span><span class="sxs-lookup"><span data-stu-id="40758-119">Specifies the name of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40758-120">-Path</span><span class="sxs-lookup"><span data-stu-id="40758-120">-Path</span></span>
<span data-ttu-id="40758-121">Gibt den Dateipfad an, zu dem dieses Cmdlet die JSON-Definition für den Wiederherstellungsplan speichert.</span><span class="sxs-lookup"><span data-stu-id="40758-121">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="40758-122">Die JSON-Definition kann bearbeitet werden, um den Wiederherstellungsplan zu ändern und den Wiederherstellungsplan über das Update-AzureRmRecoveryServicesASRRecoveryPlan-Cmdlet zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="40758-122">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40758-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40758-123">CommonParameters</span></span>
<span data-ttu-id="40758-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40758-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40758-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40758-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40758-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="40758-126">INPUTS</span></span>

### <span data-ttu-id="40758-127">Keine</span><span class="sxs-lookup"><span data-stu-id="40758-127">None</span></span>

## <span data-ttu-id="40758-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="40758-128">OUTPUTS</span></span>

### <span data-ttu-id="40758-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="40758-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="40758-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="40758-130">NOTES</span></span>

## <span data-ttu-id="40758-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="40758-131">RELATED LINKS</span></span>

[<span data-ttu-id="40758-132">Neu – AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="40758-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="40758-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="40758-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="40758-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="40758-134">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
