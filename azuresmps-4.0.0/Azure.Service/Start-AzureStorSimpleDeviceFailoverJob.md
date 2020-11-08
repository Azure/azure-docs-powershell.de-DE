---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005982"
---
# <span data-ttu-id="3ecd5-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="3ecd5-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="3ecd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ecd5-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecd5-103">Initiiert einen Failover-Vorgang von Volumen Container Gruppen.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="3ecd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ecd5-104">SYNTAX</span></span>

### <span data-ttu-id="3ecd5-105">Leer (Standard)</span><span class="sxs-lookup"><span data-stu-id="3ecd5-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3ecd5-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="3ecd5-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3ecd5-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="3ecd5-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3ecd5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ecd5-108">DESCRIPTION</span></span>
<span data-ttu-id="3ecd5-109">Das Cmdlet **Start-AzureStorSimpleDeviceFailoverJob** initiiert einen Failovervorgang einer oder mehrerer Volumen Container Gruppen von einem Gerät zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="3ecd5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ecd5-110">EXAMPLES</span></span>

### <span data-ttu-id="3ecd5-111">Beispiel 1: Starten eines Failover-Auftrags für ein benanntes Gerät und benanntes Zielgerät</span><span class="sxs-lookup"><span data-stu-id="3ecd5-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="3ecd5-112">Dieser Befehl ruft die Failover-Volumen Container für das Gerät mit dem Namen ChewD_App7 mit dem Cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** ab.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="3ecd5-113">Der Befehl übergibt die Ergebnisse an das Cmdlet **Where-Object** , in dem die Container mit einem anderen Wert als $true für die **IsDCGroupEligibleForDR** -Eigenschaft gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="3ecd5-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="3ecd5-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="3ecd5-115">Das aktuelle Cmdlet startet Failover-Aufträge für die restlichen Failover-Volumen Container.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="3ecd5-116">Der Befehl gibt den Gerätenamen und den Namen des Zielgeräts an.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="3ecd5-117">Der Befehl gibt die Instanz-ID des Auftrags zurück, den das Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="3ecd5-118">Beispiel 2: Starten eines Failover-Auftrags für ein Gerät und Zielgerät, angegeben durch die ID</span><span class="sxs-lookup"><span data-stu-id="3ecd5-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="3ecd5-119">Dieser Befehl ruft die Failover-Volumen Container für das Gerät mit dem Namen ChewD_App7 mithilfe von **Get-AzureStorSimpleFailoverVolumeContainers** ab.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="3ecd5-120">Der Befehl übergibt die Ergebnisse an **Where-Object** , wodurch diese mit einem anderen Wert als $true für die **IsDCGroupEligibleForDR** -Eigenschaft gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="3ecd5-121">Das Cmdlet übergibt die Ergebnisse an das Cmdlet **"Select-Object"** , das das erste Objekt auswählt, das an das aktuelle Cmdlet übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="3ecd5-122">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="3ecd5-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="3ecd5-123">Das aktuelle Cmdlet startet Failover-Aufträge für den ausgewählten Failover-Volumen Container.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="3ecd5-124">Der Befehl gibt die Geräte-ID und die Zielgeräte-ID an.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="3ecd5-125">Der Befehl gibt die Instanz-ID des Auftrags zurück, den das Cmdlet startet.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="3ecd5-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ecd5-126">PARAMETERS</span></span>

### <span data-ttu-id="3ecd5-127">-Geräte-Nr</span><span class="sxs-lookup"><span data-stu-id="3ecd5-127">-DeviceId</span></span>
<span data-ttu-id="3ecd5-128">Gibt die Instanz-ID des StorSimple-Geräts an, auf dem die Volumen Container Gruppen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

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

### <span data-ttu-id="3ecd5-129">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3ecd5-129">-DeviceName</span></span>
<span data-ttu-id="3ecd5-130">Gibt den Namen des StorSimple-Geräts an, auf dem die Volumen Container Gruppen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

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

### <span data-ttu-id="3ecd5-131">-Force</span><span class="sxs-lookup"><span data-stu-id="3ecd5-131">-Force</span></span>
<span data-ttu-id="3ecd5-132">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-132">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecd5-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="3ecd5-133">-Profile</span></span>
<span data-ttu-id="3ecd5-134">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="3ecd5-135">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="3ecd5-135">-TargetDeviceId</span></span>
<span data-ttu-id="3ecd5-136">Gibt die Instanz-ID des StorSimple-Geräts an, für das dieses Cmdlet einen Failover für die Volumen Container Gruppen durchführt.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

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

### <span data-ttu-id="3ecd5-137">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="3ecd5-137">-TargetDeviceName</span></span>
<span data-ttu-id="3ecd5-138">Gibt den Namen des StorSimple-Geräts an, für das dieses Cmdlet einen Failover der Volumen Container Gruppen durchführt.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

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

### <span data-ttu-id="3ecd5-139">-VolumecontainerGroups</span><span class="sxs-lookup"><span data-stu-id="3ecd5-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="3ecd5-140">Gibt die Liste der Volumen Container Gruppen an, für die dieses Cmdlet einen Failover zu einem anderen Gerät durchführt.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ecd5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecd5-141">CommonParameters</span></span>
<span data-ttu-id="3ecd5-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecd5-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecd5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecd5-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ecd5-144">INPUTS</span></span>

### <span data-ttu-id="3ecd5-145">Liste\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="3ecd5-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="3ecd5-146">Sie können eine Liste mit Volumen Container Gruppen an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="3ecd5-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="3ecd5-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ecd5-147">OUTPUTS</span></span>

### <span data-ttu-id="3ecd5-148">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="3ecd5-148">String</span></span>

## <span data-ttu-id="3ecd5-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ecd5-149">NOTES</span></span>

## <span data-ttu-id="3ecd5-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ecd5-150">RELATED LINKS</span></span>

[<span data-ttu-id="3ecd5-151">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="3ecd5-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)


