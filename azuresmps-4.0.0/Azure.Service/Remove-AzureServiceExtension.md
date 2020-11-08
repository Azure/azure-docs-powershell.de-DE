---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6B5E4968-5DF5-4956-A070-9F54A79D960B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f45e0a93b2f6261ca6031aa721bda3a72f4443dd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006319"
---
# <span data-ttu-id="5dacf-101">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="5dacf-101">Remove-AzureServiceExtension</span></span>

## <span data-ttu-id="5dacf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5dacf-102">SYNOPSIS</span></span>
<span data-ttu-id="5dacf-103">Entfernt Cloud-Diensterweiterungen, die auf eine Bereitstellung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dacf-103">Removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="5dacf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dacf-104">SYNTAX</span></span>

### <span data-ttu-id="5dacf-105">RemoveByRoles (Standard)</span><span class="sxs-lookup"><span data-stu-id="5dacf-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-ExtensionName] <String> [-ProviderNamespace] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5dacf-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="5dacf-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-UninstallConfiguration] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5dacf-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dacf-107">DESCRIPTION</span></span>
<span data-ttu-id="5dacf-108">Das Cmdlet **Remove-AzureServiceExtension** entfernt Cloud-Diensterweiterungen, die auf eine Bereitstellung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5dacf-108">The **Remove-AzureServiceExtension** cmdlet removes cloud service extensions that are applied on a deployment.</span></span>

## <span data-ttu-id="5dacf-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5dacf-109">EXAMPLES</span></span>

### <span data-ttu-id="5dacf-110">Beispiel 1: Entfernen einer Diensterweiterung</span><span class="sxs-lookup"><span data-stu-id="5dacf-110">Example 1: Remove a service extension</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions"
```

<span data-ttu-id="5dacf-111">Mit diesem Befehl wird eine Diensterweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="5dacf-111">This command removes a service extension.</span></span>

### <span data-ttu-id="5dacf-112">Beispiel 2: Entfernen einer Diensterweiterung und Deinstallieren aller Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="5dacf-112">Example 2: Remove a service extension and uninstall all configurations</span></span>
```
PS C:\> Remove-AzureServiceExtension -ServiceName $Svc -Slot "Production" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -UninstallConfiguration
```

<span data-ttu-id="5dacf-113">Mit diesem Befehl wird eine Diensterweiterung entfernt und alle Konfigurationen deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="5dacf-113">This command removes a service extension and uninstalls all configurations.</span></span>

## <span data-ttu-id="5dacf-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dacf-114">PARAMETERS</span></span>

### <span data-ttu-id="5dacf-115">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="5dacf-115">-ExtensionName</span></span>
<span data-ttu-id="5dacf-116">Gibt den Namen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="5dacf-116">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dacf-117">-Information</span><span class="sxs-lookup"><span data-stu-id="5dacf-117">-InformationAction</span></span>
<span data-ttu-id="5dacf-118">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="5dacf-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5dacf-119">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5dacf-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5dacf-120">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="5dacf-120">Continue</span></span>
- <span data-ttu-id="5dacf-121">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="5dacf-121">Ignore</span></span>
- <span data-ttu-id="5dacf-122">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="5dacf-122">Inquire</span></span>
- <span data-ttu-id="5dacf-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5dacf-123">SilentlyContinue</span></span>
- <span data-ttu-id="5dacf-124">Beenden</span><span class="sxs-lookup"><span data-stu-id="5dacf-124">Stop</span></span>
- <span data-ttu-id="5dacf-125">Anhalten</span><span class="sxs-lookup"><span data-stu-id="5dacf-125">Suspend</span></span>

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

### <span data-ttu-id="5dacf-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5dacf-126">-InformationVariable</span></span>
<span data-ttu-id="5dacf-127">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="5dacf-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5dacf-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="5dacf-128">-Profile</span></span>
<span data-ttu-id="5dacf-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5dacf-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5dacf-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5dacf-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5dacf-131">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="5dacf-131">-ProviderNamespace</span></span>
<span data-ttu-id="5dacf-132">Gibt den Namespace des Erweiterungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="5dacf-132">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dacf-133">-Role</span><span class="sxs-lookup"><span data-stu-id="5dacf-133">-Role</span></span>
<span data-ttu-id="5dacf-134">Gibt ein optionales Array von Rollen an, für die die Erweiterung angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dacf-134">Specifies an optional array of roles to specify the extension for.</span></span>
<span data-ttu-id="5dacf-135">Wenn nicht angegeben, wird die Erweiterung als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5dacf-135">If not specified the extension is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="5dacf-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5dacf-136">-ServiceName</span></span>
<span data-ttu-id="5dacf-137">Gibt den Namen des Cloud-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="5dacf-137">Specifies the cloud service name.</span></span>

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

### <span data-ttu-id="5dacf-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="5dacf-138">-Slot</span></span>
<span data-ttu-id="5dacf-139">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5dacf-139">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="5dacf-140">Gültige Werte sind Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="5dacf-140">Valid values are Production or Staging.</span></span>

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

### <span data-ttu-id="5dacf-141">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5dacf-141">-UninstallConfiguration</span></span>
<span data-ttu-id="5dacf-142">Gibt an, dass dieses Cmdlet alle Konfigurationen vom clouddienst deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="5dacf-142">Indicates that this cmdlet uninstalls all configurations from the cloud service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAllRoles
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dacf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dacf-143">CommonParameters</span></span>
<span data-ttu-id="5dacf-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dacf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dacf-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dacf-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dacf-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5dacf-146">INPUTS</span></span>

## <span data-ttu-id="5dacf-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5dacf-147">OUTPUTS</span></span>

## <span data-ttu-id="5dacf-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="5dacf-148">NOTES</span></span>

## <span data-ttu-id="5dacf-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5dacf-149">RELATED LINKS</span></span>

[<span data-ttu-id="5dacf-150">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="5dacf-150">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="5dacf-151">Satz-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="5dacf-151">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


