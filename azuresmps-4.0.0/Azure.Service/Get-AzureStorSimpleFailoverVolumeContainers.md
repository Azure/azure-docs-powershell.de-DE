---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005767"
---
# <span data-ttu-id="282af-101">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="282af-101">Get-AzureStorSimpleFailoverVolumeContainers</span></span>

## <span data-ttu-id="282af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="282af-102">SYNOPSIS</span></span>
<span data-ttu-id="282af-103">Ruft die Volumen Container Gruppen für das Geräte Failover ab.</span><span class="sxs-lookup"><span data-stu-id="282af-103">Gets the volume container groups for device failover.</span></span>

## <span data-ttu-id="282af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="282af-104">SYNTAX</span></span>

### <span data-ttu-id="282af-105">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="282af-105">IdentifyById</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="282af-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="282af-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="282af-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="282af-107">DESCRIPTION</span></span>
<span data-ttu-id="282af-108">Das Cmdlet " **Get-AzureStorSimpleFailoverVolumeContainers** " Ruft die Volumen Container Gruppen für das Geräte Failover ab.</span><span class="sxs-lookup"><span data-stu-id="282af-108">The **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet gets the volume container groups for device failover.</span></span>
<span data-ttu-id="282af-109">Übergeben Sie eine einzelne **VolumeContainer** -Gruppe oder ein Array von **VolumeContainer** -Gruppen an das Cmdlet **Start-AzureStorSimpleDeviceFailover** .</span><span class="sxs-lookup"><span data-stu-id="282af-109">Pass a single **VolumeContainer** group or an array of **VolumeContainer** groups to the **Start-AzureStorSimpleDeviceFailover** cmdlet.</span></span>
<span data-ttu-id="282af-110">Für Failover können nur Gruppen mit dem Wert $true für die **IsDCGroupEligibleForDR** -Eigenschaft ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="282af-110">Only groups that have a value of $True for the **IsDCGroupEligibleForDR** property are eligible for failover.</span></span>

## <span data-ttu-id="282af-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="282af-111">EXAMPLES</span></span>

### <span data-ttu-id="282af-112">Beispiel 1: Abrufen von Failover-Volumen Containern</span><span class="sxs-lookup"><span data-stu-id="282af-112">Example 1: Get failover volume containers</span></span>
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

<span data-ttu-id="282af-113">Dieser Befehl ruft Failover-Volumen Container ab.</span><span class="sxs-lookup"><span data-stu-id="282af-113">This command gets failover volume containers.</span></span>
<span data-ttu-id="282af-114">Für das Geräte Failover können nur die DCGroups verwendet werden, die den Wert $true für die **IsDCGroupEligibleForDR** -Eigenschaft aufweisen.</span><span class="sxs-lookup"><span data-stu-id="282af-114">Only the DCGroups that have a value of $True for the **IsDCGroupEligibleForDR** property can be used for device failover.</span></span>

## <span data-ttu-id="282af-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="282af-115">PARAMETERS</span></span>

### <span data-ttu-id="282af-116">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="282af-116">-DeviceId</span></span>
<span data-ttu-id="282af-117">Gibt die Instanz-ID des StorSimple-Geräts an, auf dem das Cmdlet ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="282af-117">Specifies the instance ID of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="282af-118">-DeviceName</span></span>
<span data-ttu-id="282af-119">Gibt den Namen des StorSimple-Geräts an, auf dem das Cmdlet ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="282af-119">Specifies the name of the StorSimple device on which to run the cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-120">-Profil</span><span class="sxs-lookup"><span data-stu-id="282af-120">-Profile</span></span>
<span data-ttu-id="282af-121">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="282af-121">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="282af-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="282af-122">CommonParameters</span></span>
<span data-ttu-id="282af-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="282af-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="282af-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="282af-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="282af-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="282af-125">INPUTS</span></span>

## <span data-ttu-id="282af-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="282af-126">OUTPUTS</span></span>

### <span data-ttu-id="282af-127">IList\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="282af-127">IList\<DataContainerGroup\></span></span>
<span data-ttu-id="282af-128">Dieses Cmdlet gibt eine Liste von **VolumeContainer** -Gruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="282af-128">This cmdlet returns a list of **VolumeContainer** groups.</span></span>

## <span data-ttu-id="282af-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="282af-129">NOTES</span></span>

## <span data-ttu-id="282af-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="282af-130">RELATED LINKS</span></span>

[<span data-ttu-id="282af-131">Anfang-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="282af-131">Start-AzureStorSimpleDeviceFailoverJob</span></span>](./Start-AzureStorSimpleDeviceFailoverJob.md)

[<span data-ttu-id="282af-132">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="282af-132">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


