---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95298AFC-B492-4EA6-AFC2-E862D3086AF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84b1256d7d911d22a4f1344bdf841943ce87ee7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006322"
---
# <span data-ttu-id="b916c-101">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b916c-101">Remove-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="b916c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b916c-102">SYNOPSIS</span></span>
<span data-ttu-id="b916c-103">Entfernt die Erweiterung für die Cloud-Dienst Diagnose, die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b916c-103">Removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="b916c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b916c-104">SYNTAX</span></span>

### <span data-ttu-id="b916c-105">RemoveByRoles (Standard)</span><span class="sxs-lookup"><span data-stu-id="b916c-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="b916c-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="b916c-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b916c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b916c-107">DESCRIPTION</span></span>
<span data-ttu-id="b916c-108">Das Cmdlet **Remove-AzureServiceDiagnosticsExtension** entfernt die auf alle Rollen oder benannten Rollen angewendete Cloud Service Diagnostics-Erweiterung in einem bestimmten Bereitstellungs Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="b916c-108">The **Remove-AzureServiceDiagnosticsExtension** cmdlet removes the cloud service diagnostics extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="b916c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b916c-109">EXAMPLES</span></span>

### <span data-ttu-id="b916c-110">Beispiel 1: Entfernen der Diagnose Erweiterung für einen Dienst</span><span class="sxs-lookup"><span data-stu-id="b916c-110">Example 1: Remove the diagnostic extension for a service</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc
```

<span data-ttu-id="b916c-111">Mit diesem Befehl wird die Diagnose Erweiterung für eine angegebene Rolle entfernt.</span><span class="sxs-lookup"><span data-stu-id="b916c-111">This command removes the diagnostic extension for a specified role.</span></span>

### <span data-ttu-id="b916c-112">Beispiel 2: Entfernen der Diagnose Erweiterung für einen Dienst in einer angegebenen Rolle</span><span class="sxs-lookup"><span data-stu-id="b916c-112">Example 2: Remove the diagnostic extension for a service in a specified role</span></span>
```
PS C:\> Remove-AzureServiceDiagnosticsExtension -ServiceName $Svc -Role "WebRole01"
```

<span data-ttu-id="b916c-113">Mit diesem Befehl wird die Diagnose Erweiterung für eine angegebene Rolle entfernt.</span><span class="sxs-lookup"><span data-stu-id="b916c-113">This command removes the diagnostic extension for a specified role.</span></span>

## <span data-ttu-id="b916c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="b916c-114">PARAMETERS</span></span>

### <span data-ttu-id="b916c-115">-Information</span><span class="sxs-lookup"><span data-stu-id="b916c-115">-InformationAction</span></span>
<span data-ttu-id="b916c-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="b916c-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b916c-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b916c-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b916c-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="b916c-118">Continue</span></span>
- <span data-ttu-id="b916c-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="b916c-119">Ignore</span></span>
- <span data-ttu-id="b916c-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="b916c-120">Inquire</span></span>
- <span data-ttu-id="b916c-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b916c-121">SilentlyContinue</span></span>
- <span data-ttu-id="b916c-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="b916c-122">Stop</span></span>
- <span data-ttu-id="b916c-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="b916c-123">Suspend</span></span>

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

### <span data-ttu-id="b916c-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b916c-124">-InformationVariable</span></span>
<span data-ttu-id="b916c-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="b916c-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b916c-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="b916c-126">-Profile</span></span>
<span data-ttu-id="b916c-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="b916c-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b916c-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="b916c-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b916c-129">-Role</span><span class="sxs-lookup"><span data-stu-id="b916c-129">-Role</span></span>
<span data-ttu-id="b916c-130">Gibt ein optionales Array von Rollen an, für das die Remote Desktopkonfiguration angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b916c-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="b916c-131">Wenn Sie diesen Parameter nicht angeben, wird die Remote Desktopkonfiguration als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b916c-131">If you do not specify this parameter, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: RemoveByRoles
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b916c-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b916c-132">-ServiceName</span></span>
<span data-ttu-id="b916c-133">Gibt den Azure-Dienstnamen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="b916c-133">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b916c-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="b916c-134">-Slot</span></span>
<span data-ttu-id="b916c-135">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b916c-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="b916c-136">Gültige Werte sind Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="b916c-136">Valid values are Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b916c-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="b916c-137">-UninstallConfiguration</span></span>
<span data-ttu-id="b916c-138">Gibt an, dass dieses Cmdlet alle RDP-Konfigurationen vom clouddienst deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="b916c-138">Indicates that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b916c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b916c-139">CommonParameters</span></span>
<span data-ttu-id="b916c-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b916c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b916c-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b916c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b916c-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b916c-142">INPUTS</span></span>

## <span data-ttu-id="b916c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b916c-143">OUTPUTS</span></span>

## <span data-ttu-id="b916c-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="b916c-144">NOTES</span></span>

## <span data-ttu-id="b916c-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b916c-145">RELATED LINKS</span></span>

[<span data-ttu-id="b916c-146">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b916c-146">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="b916c-147">Satz-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="b916c-147">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


