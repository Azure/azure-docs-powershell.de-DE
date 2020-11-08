---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006371"
---
# <span data-ttu-id="86ff4-101">Remove-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="86ff4-101">Remove-AzureDeployment</span></span>

## <span data-ttu-id="86ff4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86ff4-102">SYNOPSIS</span></span>
<span data-ttu-id="86ff4-103">Löscht eine Bereitstellungeines Cloud-Diensts.</span><span class="sxs-lookup"><span data-stu-id="86ff4-103">Deletes a deployment of a cloud service.</span></span>

## <span data-ttu-id="86ff4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86ff4-104">SYNTAX</span></span>

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="86ff4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86ff4-105">DESCRIPTION</span></span>
<span data-ttu-id="86ff4-106">Das Cmdlet **Remove-AzureDeployment** löscht eine Bereitstellungeines Azure Cloud-Diensts.</span><span class="sxs-lookup"><span data-stu-id="86ff4-106">The **Remove-AzureDeployment** cmdlet deletes a deployment of an Azure cloud service.</span></span>
<span data-ttu-id="86ff4-107">Wenn Sie eine Bereitstellung löschen möchten, müssen Sie Sie zuerst anhalten.</span><span class="sxs-lookup"><span data-stu-id="86ff4-107">To delete a deployment, first suspend it.</span></span>

## <span data-ttu-id="86ff4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86ff4-108">EXAMPLES</span></span>

### <span data-ttu-id="86ff4-109">Beispiel 1: Entfernen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="86ff4-109">Example 1: Remove a deployment</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

<span data-ttu-id="86ff4-110">Dieser Befehl entfernt die Bereitstellung des Azure-Diensts mit dem Namen ContosoService.</span><span class="sxs-lookup"><span data-stu-id="86ff4-110">This command removes the deployment of the Azure service named ContosoService.</span></span>
<span data-ttu-id="86ff4-111">Da dieser Befehl keinen Steckplatz angibt, wird der Dienst aus der Produktionsumgebung entfernt.</span><span class="sxs-lookup"><span data-stu-id="86ff4-111">Because this command does not specify a slot, it removes the service from the production environment.</span></span>

### <span data-ttu-id="86ff4-112">Beispiel 2: Entfernen einer Bereitstellung und virtueller Festplatten</span><span class="sxs-lookup"><span data-stu-id="86ff4-112">Example 2: Remove a deployment and virtual hard disks</span></span>
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

<span data-ttu-id="86ff4-113">Mit diesem Befehl wird die Bereitstellung des Diensts mit dem Namen ContosoService aus der Produktionsumgebung entfernt.</span><span class="sxs-lookup"><span data-stu-id="86ff4-113">This command removes the deployment of the service named ContosoService from the production environment.</span></span>
<span data-ttu-id="86ff4-114">Der Befehl entfernt auch die zugrunde liegenden virtuellen Festplatten.</span><span class="sxs-lookup"><span data-stu-id="86ff4-114">The command also removes the underlying virtual hard disks.</span></span>

## <span data-ttu-id="86ff4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="86ff4-115">PARAMETERS</span></span>

### <span data-ttu-id="86ff4-116">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="86ff4-116">-DeleteVHD</span></span>
<span data-ttu-id="86ff4-117">Gibt an, dass dieses Cmdlet die Bereitstellung und die virtuellen Festplatten (VHD) aus dem BLOB-Speicher entfernt.</span><span class="sxs-lookup"><span data-stu-id="86ff4-117">Specifies that this cmdlet removes the deployment and the virtual hard disks (VHDs) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ff4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="86ff4-118">-Force</span></span>
<span data-ttu-id="86ff4-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="86ff4-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ff4-120">-Information</span><span class="sxs-lookup"><span data-stu-id="86ff4-120">-InformationAction</span></span>
<span data-ttu-id="86ff4-121">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="86ff4-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="86ff4-122">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="86ff4-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="86ff4-123">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="86ff4-123">Continue</span></span>
- <span data-ttu-id="86ff4-124">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="86ff4-124">Ignore</span></span>
- <span data-ttu-id="86ff4-125">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="86ff4-125">Inquire</span></span>
- <span data-ttu-id="86ff4-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="86ff4-126">SilentlyContinue</span></span>
- <span data-ttu-id="86ff4-127">Beenden</span><span class="sxs-lookup"><span data-stu-id="86ff4-127">Stop</span></span>
- <span data-ttu-id="86ff4-128">Anhalten</span><span class="sxs-lookup"><span data-stu-id="86ff4-128">Suspend</span></span>

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

### <span data-ttu-id="86ff4-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="86ff4-129">-InformationVariable</span></span>
<span data-ttu-id="86ff4-130">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="86ff4-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="86ff4-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="86ff4-131">-Profile</span></span>
<span data-ttu-id="86ff4-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="86ff4-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="86ff4-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="86ff4-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="86ff4-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="86ff4-134">-ServiceName</span></span>
<span data-ttu-id="86ff4-135">Gibt den Namen des Diensts an, für den das Cmdlet eine Bereitstellung löscht.</span><span class="sxs-lookup"><span data-stu-id="86ff4-135">Specifies the name of the service for which this cmdlet deletes a deployment.</span></span>

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

### <span data-ttu-id="86ff4-136">-Slot</span><span class="sxs-lookup"><span data-stu-id="86ff4-136">-Slot</span></span>
<span data-ttu-id="86ff4-137">Gibt die Bereitstellungsumgebung an, aus der dieses Cmdlet die Bereitstellung löscht.</span><span class="sxs-lookup"><span data-stu-id="86ff4-137">Specifies the deployment environment from which this cmdlet deletes the deployment.</span></span>
<span data-ttu-id="86ff4-138">Gültige Werte sind: Staging und Production.</span><span class="sxs-lookup"><span data-stu-id="86ff4-138">Valid values are: Staging and Production.</span></span>
<span data-ttu-id="86ff4-139">Der Standardwert ist Production.</span><span class="sxs-lookup"><span data-stu-id="86ff4-139">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ff4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ff4-140">CommonParameters</span></span>
<span data-ttu-id="86ff4-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ff4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ff4-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ff4-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ff4-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86ff4-143">INPUTS</span></span>

## <span data-ttu-id="86ff4-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86ff4-144">OUTPUTS</span></span>

### <span data-ttu-id="86ff4-145">ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="86ff4-145">ManagementOperationContext</span></span>

## <span data-ttu-id="86ff4-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="86ff4-146">NOTES</span></span>

## <span data-ttu-id="86ff4-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86ff4-147">RELATED LINKS</span></span>

[<span data-ttu-id="86ff4-148">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="86ff4-148">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="86ff4-149">Get-AzureDeploymentEvent</span><span class="sxs-lookup"><span data-stu-id="86ff4-149">Get-AzureDeploymentEvent</span></span>](./Get-AzureDeploymentEvent.md)

[<span data-ttu-id="86ff4-150">Verschieben-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="86ff4-150">Move-AzureDeployment</span></span>](./Move-AzureDeployment.md)

[<span data-ttu-id="86ff4-151">Neu – AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="86ff4-151">New-AzureDeployment</span></span>](./New-AzureDeployment.md)

[<span data-ttu-id="86ff4-152">Satz-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="86ff4-152">Set-AzureDeployment</span></span>](./Set-AzureDeployment.md)


