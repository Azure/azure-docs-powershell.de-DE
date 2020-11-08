---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8A6B2633-EECC-416A-85F6-69C8341AA970
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82ef50dcdf5f17e044a9dc2091cbfda5cb5d1b2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005826"
---
# <span data-ttu-id="ed349-101">Get-AzureRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="ed349-101">Get-AzureRemoteDesktopFile</span></span>

## <span data-ttu-id="ed349-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed349-102">SYNOPSIS</span></span>
<span data-ttu-id="ed349-103">Ruft eine RDP-Datei für einen virtuellen Azure-Computer ab.</span><span class="sxs-lookup"><span data-stu-id="ed349-103">Gets an RDP file for an Azure virtual machine.</span></span>

## <span data-ttu-id="ed349-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed349-104">SYNTAX</span></span>

### <span data-ttu-id="ed349-105">Download (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed349-105">Download (Default)</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [-LocalPath] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed349-106">Starten</span><span class="sxs-lookup"><span data-stu-id="ed349-106">Launch</span></span>
```
Get-AzureRemoteDesktopFile [-Name] <String> [[-LocalPath] <String>] [-Launch] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed349-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed349-107">DESCRIPTION</span></span>
<span data-ttu-id="ed349-108">Das Cmdlet " **Get-AzureRemoteDesktopFile** " downloadet und speichert eine RDP-Datei (Remote Desktop Connection) für einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="ed349-108">The **Get-AzureRemoteDesktopFile** cmdlet downloads and saves a remote desktop connection (RDP) file for an Azure virtual machine.</span></span>
<span data-ttu-id="ed349-109">Mit dem Cmdlet kann eine Remotedesktopverbindung mit dem angegebenen virtuellen Computer gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="ed349-109">The cmdlet can launch a remote desktop connection to the specified virtual machine.</span></span>

## <span data-ttu-id="ed349-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed349-110">EXAMPLES</span></span>

### <span data-ttu-id="ed349-111">Beispiel 1: Abrufen einer RDP-Datei</span><span class="sxs-lookup"><span data-stu-id="ed349-111">Example 1: Get an RDP file</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -LocalPath "C:\temp\VirtualMachine07.rdp"
```

<span data-ttu-id="ed349-112">Dieser Befehl ruft eine RDP-Datei für den virtuellen VirtualMachine07-Computer mit dem Namen VirtualMachine07 ab, der auf dem Dienst mit dem Namen ContosoService ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed349-112">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="ed349-113">Der Befehl speichert diese Datei als C:\temp\VirtualMachine07.RDP.</span><span class="sxs-lookup"><span data-stu-id="ed349-113">The command stores that file as C:\temp\VirtualMachine07.rdp.</span></span>

### <span data-ttu-id="ed349-114">Beispiel 2: Starten einer Remotesitzung</span><span class="sxs-lookup"><span data-stu-id="ed349-114">Example 2: Start a remote session</span></span>
```
PS C:\> Get-AzureRemoteDesktopFile -ServiceName "ContosoService" -Name "VirtualMachine07" -Launch
```

<span data-ttu-id="ed349-115">Dieser Befehl ruft eine RDP-Datei für den virtuellen VirtualMachine07-Computer mit dem Namen VirtualMachine07 ab, der auf dem Dienst mit dem Namen ContosoService ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed349-115">This command gets an RDP file for the VirtualMachine07 virtual machine named VirtualMachine07 that runs on the service named ContosoService.</span></span>
<span data-ttu-id="ed349-116">Der Befehl startet eine Remotedesktopsitzung.</span><span class="sxs-lookup"><span data-stu-id="ed349-116">The command launches a remote desktop session.</span></span>
<span data-ttu-id="ed349-117">Der Befehl löscht die RDP-Datei, wenn die Verbindung geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="ed349-117">The command deletes the RDP file when the connection is closed.</span></span>

## <span data-ttu-id="ed349-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed349-118">PARAMETERS</span></span>

### <span data-ttu-id="ed349-119">-Information</span><span class="sxs-lookup"><span data-stu-id="ed349-119">-InformationAction</span></span>
<span data-ttu-id="ed349-120">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="ed349-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ed349-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ed349-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ed349-122">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="ed349-122">Continue</span></span>
- <span data-ttu-id="ed349-123">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="ed349-123">Ignore</span></span>
- <span data-ttu-id="ed349-124">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="ed349-124">Inquire</span></span>
- <span data-ttu-id="ed349-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ed349-125">SilentlyContinue</span></span>
- <span data-ttu-id="ed349-126">Beenden</span><span class="sxs-lookup"><span data-stu-id="ed349-126">Stop</span></span>
- <span data-ttu-id="ed349-127">Anhalten</span><span class="sxs-lookup"><span data-stu-id="ed349-127">Suspend</span></span>

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

### <span data-ttu-id="ed349-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ed349-128">-InformationVariable</span></span>
<span data-ttu-id="ed349-129">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="ed349-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ed349-130">-Start</span><span class="sxs-lookup"><span data-stu-id="ed349-130">-Launch</span></span>
<span data-ttu-id="ed349-131">Gibt an, dass mit diesem Cmdlet eine Remotedesktopsitzung mit dem virtuellen Computer gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ed349-131">Indicates that this cmdlet starts a remote desktop session to the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed349-132">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="ed349-132">-LocalPath</span></span>
<span data-ttu-id="ed349-133">Gibt den vollständigen Pfad der heruntergeladenen RDP-Datei auf dem lokalen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ed349-133">Specifies the full path of the downloaded RDP file on the local computer.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed349-134">-Name</span><span class="sxs-lookup"><span data-stu-id="ed349-134">-Name</span></span>
<span data-ttu-id="ed349-135">Gibt den virtuellen Computer an, für den dieses Cmdlet eine RDP-Datei herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="ed349-135">Specifies the virtual machine for which this cmdlet downloads an RDP file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: InstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed349-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="ed349-136">-Profile</span></span>
<span data-ttu-id="ed349-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ed349-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ed349-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ed349-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ed349-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ed349-139">-ServiceName</span></span>
<span data-ttu-id="ed349-140">Gibt den Namen des Azure-Diensts an, zu dem der virtuelle Computer gehört.</span><span class="sxs-lookup"><span data-stu-id="ed349-140">Specifies the name of the Azure service to which the virtual machine belongs.</span></span>

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

### <span data-ttu-id="ed349-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed349-141">CommonParameters</span></span>
<span data-ttu-id="ed349-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed349-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed349-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed349-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed349-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed349-144">INPUTS</span></span>

## <span data-ttu-id="ed349-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed349-145">OUTPUTS</span></span>

## <span data-ttu-id="ed349-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed349-146">NOTES</span></span>

## <span data-ttu-id="ed349-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed349-147">RELATED LINKS</span></span>

