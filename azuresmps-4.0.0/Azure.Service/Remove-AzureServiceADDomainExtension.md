---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A280C0B-5F55-4575-9B11-596F497C4305
online version: ''
schema: 2.0.0
ms.openlocfilehash: 71e49425724926848ee69b24f5dfca70df664913
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006332"
---
# <span data-ttu-id="9152e-101">Remove-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="9152e-101">Remove-AzureServiceADDomainExtension</span></span>

## <span data-ttu-id="9152e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9152e-102">SYNOPSIS</span></span>
<span data-ttu-id="9152e-103">Entfernt die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendete Active Directory-Domänenerweiterung für Cloud-Dienst.</span><span class="sxs-lookup"><span data-stu-id="9152e-103">Removes the cloud service AD domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="9152e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9152e-104">SYNTAX</span></span>

### <span data-ttu-id="9152e-105">RemoveByRoles (Standard)</span><span class="sxs-lookup"><span data-stu-id="9152e-105">RemoveByRoles (Default)</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="9152e-106">RemoveAllRoles</span><span class="sxs-lookup"><span data-stu-id="9152e-106">RemoveAllRoles</span></span>
```
Remove-AzureServiceADDomainExtension [[-ServiceName] <String>] [[-Slot] <String>] [-UninstallConfiguration]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="9152e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9152e-107">DESCRIPTION</span></span>
<span data-ttu-id="9152e-108">Das Cmdlet **Remove-AzureServiceADDomainExtension** entfernt die Active Directory (AD)-Domänenerweiterung des Cloud-Diensts, die für alle Rollen oder benannten Rollen in einem bestimmten Bereitstellungs Steckplatz angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9152e-108">The **Remove-AzureServiceADDomainExtension** cmdlet removes the cloud service Active Directory (AD) domain extension applied on all roles or named roles at a certain deployment slot.</span></span>

## <span data-ttu-id="9152e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9152e-109">EXAMPLES</span></span>

### <span data-ttu-id="9152e-110">Beispiel 1: Entfernen einer AD-Domänenerweiterung</span><span class="sxs-lookup"><span data-stu-id="9152e-110">Example 1: Remove an AD domain extension</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc
```

<span data-ttu-id="9152e-111">Mit diesem Befehl wird die von der $SVC-Variable angegebene Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="9152e-111">This command removes the extension specified by the $Svc variable.</span></span>

### <span data-ttu-id="9152e-112">Beispiel 2: Entfernen einer AD-Domänenerweiterung für eine angegebene Rolle</span><span class="sxs-lookup"><span data-stu-id="9152e-112">Example 2: Remove an AD Domain extension for a specified role</span></span>
```
PS C:\> Remove-AzureServiceADDomainExtension -ServiceName $Svc -Role "WebRole1"
```

<span data-ttu-id="9152e-113">Mit diesem Befehl wird die Diensterweiterung für die angegebene Rolle entfernt.</span><span class="sxs-lookup"><span data-stu-id="9152e-113">This command removes the service extension for the specified role.</span></span>

## <span data-ttu-id="9152e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9152e-114">PARAMETERS</span></span>

### <span data-ttu-id="9152e-115">-Information</span><span class="sxs-lookup"><span data-stu-id="9152e-115">-InformationAction</span></span>
<span data-ttu-id="9152e-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="9152e-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9152e-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9152e-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9152e-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="9152e-118">Continue</span></span>
- <span data-ttu-id="9152e-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="9152e-119">Ignore</span></span>
- <span data-ttu-id="9152e-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="9152e-120">Inquire</span></span>
- <span data-ttu-id="9152e-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9152e-121">SilentlyContinue</span></span>
- <span data-ttu-id="9152e-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="9152e-122">Stop</span></span>
- <span data-ttu-id="9152e-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="9152e-123">Suspend</span></span>

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

### <span data-ttu-id="9152e-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9152e-124">-InformationVariable</span></span>
<span data-ttu-id="9152e-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="9152e-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9152e-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="9152e-126">-Profile</span></span>
<span data-ttu-id="9152e-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9152e-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9152e-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9152e-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9152e-129">-Role</span><span class="sxs-lookup"><span data-stu-id="9152e-129">-Role</span></span>
<span data-ttu-id="9152e-130">Gibt ein optionales Array von Rollen an, für das die Remote Desktopkonfiguration angegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="9152e-130">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="9152e-131">Wenn Sie nicht angegeben wird, wird die AD-Domänenkonfiguration als Standardkonfiguration für alle Rollen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9152e-131">If not specified, the AD domain configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="9152e-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9152e-132">-ServiceName</span></span>
<span data-ttu-id="9152e-133">Gibt den Namen eines Azure-Diensts an.</span><span class="sxs-lookup"><span data-stu-id="9152e-133">Specifies the name of an Azure service.</span></span>

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

### <span data-ttu-id="9152e-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="9152e-134">-Slot</span></span>
<span data-ttu-id="9152e-135">Gibt die Umgebung der Bereitstellung an, die geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9152e-135">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="9152e-136">Gültige Werte sind: Production oder Staging.</span><span class="sxs-lookup"><span data-stu-id="9152e-136">Valid values are: Production or Staging.</span></span>

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

### <span data-ttu-id="9152e-137">-UninstallConfiguration</span><span class="sxs-lookup"><span data-stu-id="9152e-137">-UninstallConfiguration</span></span>
<span data-ttu-id="9152e-138">Gibt an, dass dieses Cmdlet alle AD-Domänenkonfigurationen aus dem clouddienst deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="9152e-138">Indicates that this cmdlet uninstalls all AD domain configurations from the cloud service.</span></span>

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

### <span data-ttu-id="9152e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9152e-139">CommonParameters</span></span>
<span data-ttu-id="9152e-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9152e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9152e-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9152e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9152e-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9152e-142">INPUTS</span></span>

## <span data-ttu-id="9152e-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9152e-143">OUTPUTS</span></span>

## <span data-ttu-id="9152e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9152e-144">NOTES</span></span>

## <span data-ttu-id="9152e-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9152e-145">RELATED LINKS</span></span>

[<span data-ttu-id="9152e-146">Get-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="9152e-146">Get-AzureServiceADDomainExtension</span></span>](./Get-AzureServiceADDomainExtension.md)

[<span data-ttu-id="9152e-147">Satz-AzureServiceADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="9152e-147">Set-AzureServiceADDomainExtension</span></span>](./Set-AzureServiceADDomainExtension.md)


