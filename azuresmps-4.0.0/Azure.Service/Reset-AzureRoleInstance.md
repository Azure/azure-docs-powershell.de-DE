---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005686"
---
# <span data-ttu-id="962d4-101">Reset-AzureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="962d4-101">Reset-AzureRoleInstance</span></span>

## <span data-ttu-id="962d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="962d4-102">SYNOPSIS</span></span>
<span data-ttu-id="962d4-103">Fordert einen Neustart oder eine Neubildung einer einzelnen Rolleninstanz oder aller Rolleninstanzen einer bestimmten Rolle an.</span><span class="sxs-lookup"><span data-stu-id="962d4-103">Requests a reboot or reimage of a single role instance or all role instances of a specific role.</span></span>

## <span data-ttu-id="962d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="962d4-104">SYNTAX</span></span>

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="962d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="962d4-105">DESCRIPTION</span></span>
<span data-ttu-id="962d4-106">Das Cmdlet **Reset-AzureRoleInstance** fordert einen Neustart oder ein reimage einer Rolleninstanz an, die in einer Bereitstellung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="962d4-106">The **Reset-AzureRoleInstance** cmdlet requests a reboot or a reimage of a role instance that is running in a deployment.</span></span>
<span data-ttu-id="962d4-107">Dieser Vorgang wird synchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="962d4-107">This operation executes synchronously.</span></span>
<span data-ttu-id="962d4-108">Wenn Sie eine Rolleninstanz neu starten, nimmt Azure die Instanz offline, startet das zugrunde liegende Betriebssystem für diese Instanz neu und führt die Instanz wieder online.</span><span class="sxs-lookup"><span data-stu-id="962d4-108">When you reboot a role instance, Azure takes the instance offline, restarts the underlying operating system for that instance, and brings the instance back online.</span></span>
<span data-ttu-id="962d4-109">Alle Daten, die auf die lokale Festplatte geschrieben werden, bleiben über einen Neustart erhalten.</span><span class="sxs-lookup"><span data-stu-id="962d4-109">Any data that is written to the local disk persists across reboots.</span></span>
<span data-ttu-id="962d4-110">Alle im Arbeitsspeicher befindlichen Daten gehen verloren.</span><span class="sxs-lookup"><span data-stu-id="962d4-110">Any data that is in-memory is lost.</span></span>

<span data-ttu-id="962d4-111">Das umbilden einer Rolleninstanz führt je nach Art der Rolle zu einem anderen Verhalten.</span><span class="sxs-lookup"><span data-stu-id="962d4-111">Reimaging a role instance results in different behavior depending on the type of role.</span></span>
<span data-ttu-id="962d4-112">Bei einer Web-oder Worker-Rolle übernimmt Azure die Rolle offline und schreibt eine Neuinstallation des Azure Guest-Betriebssystems auf den virtuellen Computer, wenn die Rolle neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="962d4-112">For a web or worker role, when the role is reimaged, Azure takes the role offline and writes a fresh installation of the Azure guest operating system to the virtual machine.</span></span>
<span data-ttu-id="962d4-113">Die Rolle wird dann wieder online geschaltet.</span><span class="sxs-lookup"><span data-stu-id="962d4-113">The role is then brought back online.</span></span>
<span data-ttu-id="962d4-114">Bei einer VM-Rolle übernimmt Azure beim erneuten abbilden der Rolle die Rolle offline, wendet das von Ihnen bereitgestellte benutzerdefinierte Bild erneut an und bringt die Rolle wieder online.</span><span class="sxs-lookup"><span data-stu-id="962d4-114">For a VM role, when the role is reimaged, Azure takes the role offline, reapplies the custom image that you provided for it, and brings the role back online.</span></span>

<span data-ttu-id="962d4-115">Azure versucht, beim erneuten abbilden der Rolle Daten in allen lokalen Speicherressourcen zu verwalten. bei einem vorübergehenden Hardwarefehler kann die lokale Speicherressource jedoch verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="962d4-115">Azure attempts to maintain data in any local storage resources when the role is reimaged; however, in case of a transient hardware failure, the local storage resource may be lost.</span></span>
<span data-ttu-id="962d4-116">Wenn für Ihre Anwendung die Beibehaltung von Daten erforderlich ist, empfiehlt es sich, in eine dauerhafte Datenquelle zu schreiben, beispielsweise ein Azure-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="962d4-116">If your application requires that data persist, writing to a durable data source, such as an Azure drive, is recommended.</span></span>
<span data-ttu-id="962d4-117">Alle Daten, die in ein lokales Verzeichnis geschrieben werden, die nicht von der lokalen Speicherressource definiert sind, gehen beim erneuten abbilden der Rolle verloren.</span><span class="sxs-lookup"><span data-stu-id="962d4-117">Any data that is written to a local directory other than that defined by the local storage resource will be lost when the role is reimaged.</span></span>

## <span data-ttu-id="962d4-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="962d4-118">EXAMPLES</span></span>

### <span data-ttu-id="962d4-119">Beispiel 1: Starten einer Rolleninstanz</span><span class="sxs-lookup"><span data-stu-id="962d4-119">Example 1: Reboot a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

<span data-ttu-id="962d4-120">Mit diesem Befehl wird die Rolleninstanz mit dem Namen MyWebRole_IN_0 in der Staging-Bereitstellung des MySvc01-Diensts neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="962d4-120">This command reboots the role instance named MyWebRole_IN_0 in the staging deployment of the MySvc01 service.</span></span>

### <span data-ttu-id="962d4-121">Beispiel 2: umbilden einer Rolleninstanz</span><span class="sxs-lookup"><span data-stu-id="962d4-121">Example 2: Reimage a role instance</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

<span data-ttu-id="962d4-122">Mit diesem Befehl werden die Rolleninstanzen in der Staging-Bereitstellung des MySvc01-Cloud-Diensts erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="962d4-122">This command reimages the role instances in the staging deployment of the MySvc01 cloud service.</span></span>

### <span data-ttu-id="962d4-123">Beispiel 3: umbilden aller Rolleninstanzen</span><span class="sxs-lookup"><span data-stu-id="962d4-123">Example 3: Reimage all role instances</span></span>
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

<span data-ttu-id="962d4-124">Mit diesem Befehl werden alle Rolleninstanzen in der Produktionsbereitstellung des MySvc01-Diensts erneut abbildet.</span><span class="sxs-lookup"><span data-stu-id="962d4-124">This command reimages all role instances in the production deployment of the MySvc01 service.</span></span>

## <span data-ttu-id="962d4-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="962d4-125">PARAMETERS</span></span>

### <span data-ttu-id="962d4-126">-Information</span><span class="sxs-lookup"><span data-stu-id="962d4-126">-InformationAction</span></span>
<span data-ttu-id="962d4-127">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="962d4-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="962d4-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="962d4-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="962d4-129">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="962d4-129">Continue</span></span>
- <span data-ttu-id="962d4-130">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="962d4-130">Ignore</span></span>
- <span data-ttu-id="962d4-131">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="962d4-131">Inquire</span></span>
- <span data-ttu-id="962d4-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="962d4-132">SilentlyContinue</span></span>
- <span data-ttu-id="962d4-133">Beenden</span><span class="sxs-lookup"><span data-stu-id="962d4-133">Stop</span></span>
- <span data-ttu-id="962d4-134">Anhalten</span><span class="sxs-lookup"><span data-stu-id="962d4-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="962d4-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="962d4-135">-InformationVariable</span></span>
<span data-ttu-id="962d4-136">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="962d4-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="962d4-137">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="962d4-137">-InstanceName</span></span>
<span data-ttu-id="962d4-138">Gibt den Namen der Rolleninstanz an, die neu abbilden oder neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="962d4-138">Specifies the name of the role instance to reimage or reboot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962d4-139">-Profil</span><span class="sxs-lookup"><span data-stu-id="962d4-139">-Profile</span></span>
<span data-ttu-id="962d4-140">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="962d4-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="962d4-141">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="962d4-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="962d4-142">-Reboot</span><span class="sxs-lookup"><span data-stu-id="962d4-142">-Reboot</span></span>
<span data-ttu-id="962d4-143">Gibt an, dass dieses Cmdlet die angegebene Rolleninstanz neu startet oder, falls keine angegeben ist, alle Rolleninstanzen.</span><span class="sxs-lookup"><span data-stu-id="962d4-143">Specifies that this cmdlet reboots the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="962d4-144">Sie müssen entweder einen *Neustart* -oder einen *reimage* -Parameter angeben, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="962d4-144">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962d4-145">-Reimage</span><span class="sxs-lookup"><span data-stu-id="962d4-145">-Reimage</span></span>
<span data-ttu-id="962d4-146">Gibt an, dass dieses Cmdlet die angegebene Rolleninstanz oder, falls keine angegeben ist, alle Rolleninstanzen umbildet.</span><span class="sxs-lookup"><span data-stu-id="962d4-146">Specifies that this cmdlet reimages the specified role instance or, if none is specified, all role instances.</span></span>
<span data-ttu-id="962d4-147">Sie müssen entweder einen *Neustart* -oder einen *reimage* -Parameter angeben, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="962d4-147">You must include either a *Reboot* or *Reimage* parameter, but not both.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962d4-148">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="962d4-148">-ServiceName</span></span>
<span data-ttu-id="962d4-149">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="962d4-149">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962d4-150">-Slot</span><span class="sxs-lookup"><span data-stu-id="962d4-150">-Slot</span></span>
<span data-ttu-id="962d4-151">Gibt die Bereitstellungsumgebung an, in der die Rolleninstanzen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="962d4-151">Specifies the deployment environment where the role instances run.</span></span>
<span data-ttu-id="962d4-152">Gültige Werte sind: Production und Staging.</span><span class="sxs-lookup"><span data-stu-id="962d4-152">Valid values are: Production and Staging.</span></span>
<span data-ttu-id="962d4-153">Sie können entweder den Parameter *deploymentname* oder *Slot* angeben, aber nicht beide.</span><span class="sxs-lookup"><span data-stu-id="962d4-153">You can include either the *DeploymentName* or *Slot* parameter, but not both.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="962d4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962d4-154">CommonParameters</span></span>
<span data-ttu-id="962d4-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="962d4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962d4-156">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="962d4-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962d4-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="962d4-157">INPUTS</span></span>

## <span data-ttu-id="962d4-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="962d4-158">OUTPUTS</span></span>

## <span data-ttu-id="962d4-159">Notizen</span><span class="sxs-lookup"><span data-stu-id="962d4-159">NOTES</span></span>

## <span data-ttu-id="962d4-160">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="962d4-160">RELATED LINKS</span></span>

[<span data-ttu-id="962d4-161">Satz-AzureRole</span><span class="sxs-lookup"><span data-stu-id="962d4-161">Set-AzureRole</span></span>](./Set-AzureRole.md)


