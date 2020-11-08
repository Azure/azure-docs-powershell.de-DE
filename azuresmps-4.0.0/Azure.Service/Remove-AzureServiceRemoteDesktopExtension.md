---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C263CCAD-E51F-420E-9AD4-4FAC09C99CB1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3c10a7694034fe4400ed415891e74f7089ce8558
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006318"
---
# <span data-ttu-id="41626-101">Remove-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="41626-101">Remove-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="41626-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="41626-102">SYNOPSIS</span></span>
<span data-ttu-id="41626-103">Entfernt die auf alle Rollen oder benannten Rollen angewendete Cloud-Dienst-Remote Desktop Erweiterung in einem angegebenen Bereitstellungs Steckplatz.</span><span class="sxs-lookup"><span data-stu-id="41626-103">Removes the cloud service remote desktop extension applied on all roles or named roles at a specified deployment slot.</span></span>

## <span data-ttu-id="41626-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="41626-104">SYNTAX</span></span>

### <span data-ttu-id="41626-105">RemoveByRoles (Standard)</span><span class="sxs-lookup"><span data-stu-id="41626-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="41626-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="41626-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-UninstallConfiguration] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="41626-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41626-107">DESCRIPTION</span></span>
<span data-ttu-id="41626-108">Das Cmdlet **Remove-AzureServiceRemoteDesktopExtension** entfernt die Remote Desktop Erweiterung des Cloud-Diensts, die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="41626-108">The **Remove-AzureServiceRemoteDesktopExtension** cmdlet removes the cloud service remote desktop extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="41626-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="41626-109">EXAMPLES</span></span>

### <span data-ttu-id="41626-110">Beispiel 1: Entfernen der Remote Desktop Erweiterung</span><span class="sxs-lookup"><span data-stu-id="41626-110">Example 1: Remove the remote desktop extension</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc
```

<span data-ttu-id="41626-111">Mit diesem Befehl wird die Remote Desktop Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="41626-111">This command removes the remote desktop extension.</span></span>

### <span data-ttu-id="41626-112">Beispiel 2: Entfernen der Remote Desktop Erweiterung von einer angegebenen Rolle</span><span class="sxs-lookup"><span data-stu-id="41626-112">Example 2: Remove the remote desktop extension from a specified role</span></span>
```
PS C:\> Remove-AzureServiceRemoteDesktopExtension -ServiceName $svc -Role "WebRole1"
```

<span data-ttu-id="41626-113">Mit diesem Befehl wird die Remote Desktop Erweiterung von einer angegebenen Rolle entfernt.</span><span class="sxs-lookup"><span data-stu-id="41626-113">This command removes the remote desktop extension from a specified role.</span></span>

## <span data-ttu-id="41626-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="41626-114">PARAMETERS</span></span>

### <span data-ttu-id="41626-115">-Information</span><span class="sxs-lookup"><span data-stu-id="41626-115">-InformationAction</span></span>
<span data-ttu-id="41626-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="41626-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="41626-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="41626-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41626-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="41626-118">Continue</span></span>
- <span data-ttu-id="41626-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="41626-119">Ignore</span></span>
- <span data-ttu-id="41626-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="41626-120">Inquire</span></span>
- <span data-ttu-id="41626-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="41626-121">SilentlyContinue</span></span>
- <span data-ttu-id="41626-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="41626-122">Stop</span></span>
- <span data-ttu-id="41626-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="41626-123">Suspend</span></span>

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

### <span data-ttu-id="41626-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="41626-124">-InformationVariable</span></span>
<span data-ttu-id="41626-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="41626-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="41626-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="41626-126">-Profile</span></span>
<span data-ttu-id="41626-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="41626-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41626-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="41626-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41626-129">-Role</span><span class="sxs-lookup"><span data-stu-id="41626-129">-Role</span></span>
<span data-ttu-id="41626-130">Gibt ein optionales Array von Rollen an, für die die Remote Desktopkonfiguration angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="41626-130">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="41626-131">Wenn nicht angegeben, wird die Remote Desktopkonfiguration als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="41626-131">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="41626-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="41626-132">-ServiceName</span></span>
<span data-ttu-id="41626-133">Gibt den Azure-Dienstnamen der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="41626-133">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="41626-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="41626-134">-Slot</span></span>
<span data-ttu-id="41626-135">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="41626-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="41626-136">Unterstützte Werte sind "Production" oder "Staging".</span><span class="sxs-lookup"><span data-stu-id="41626-136">Supported values are "Production" or "Staging".</span></span>

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

### <span data-ttu-id="41626-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="41626-137">-UninstallConfiguration</span></span>
<span data-ttu-id="41626-138">Gibt an, dass dieses Cmdlet alle RDP-Konfigurationen aus dem clouddienst deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="41626-138">Specifies that this cmdlet uninstalls all RDP configurations from the cloud service.</span></span>

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

### <span data-ttu-id="41626-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41626-139">CommonParameters</span></span>
<span data-ttu-id="41626-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41626-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41626-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41626-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41626-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="41626-142">INPUTS</span></span>

## <span data-ttu-id="41626-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="41626-143">OUTPUTS</span></span>

## <span data-ttu-id="41626-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="41626-144">NOTES</span></span>

## <span data-ttu-id="41626-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="41626-145">RELATED LINKS</span></span>

[<span data-ttu-id="41626-146">Satz-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="41626-146">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


