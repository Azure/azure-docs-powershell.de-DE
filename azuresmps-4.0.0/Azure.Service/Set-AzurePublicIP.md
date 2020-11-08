---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006161"
---
# <span data-ttu-id="4f29b-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="4f29b-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="4f29b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f29b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f29b-103">Fügt eine öffentliche IP-Adresse zu einem Azure Virtual Machine hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f29b-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="4f29b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f29b-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4f29b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f29b-105">DESCRIPTION</span></span>
<span data-ttu-id="4f29b-106">Das Cmdlet " **Satz-AzurePublicIP** " fügt eine öffentliche IP-Adresse zu einem Azure-virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f29b-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="4f29b-107">Wenn Sie dieses Cmdlet für einen vorhandenen virtuellen Computer ausführen, aktualisieren Sie den virtuellen Computer, um Ihre Änderungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="4f29b-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="4f29b-108">Sie können ein Domain Name-Label angeben, um einen entsprechenden DNS-Eintrag für die öffentliche IP-Adresse zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f29b-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="4f29b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f29b-109">EXAMPLES</span></span>

### <span data-ttu-id="4f29b-110">Beispiel 1: Hinzufügen einer öffentlichen IP zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="4f29b-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="4f29b-111">Dieser Befehl ruft den virtuellen Computer mit dem Namen FTPInstance im Dienst FTPInAzure mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="4f29b-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="4f29b-112">Der Befehl übergibt diesen virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f29b-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4f29b-113">Das aktuelle Cmdlet fügt den öffentlichen IP-Namen ftpip hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f29b-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="4f29b-114">Der Befehl übergibt den virtuellen Computer an das Cmdlet **Update-AzureVM** , das Ihre Änderungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="4f29b-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="4f29b-115">Beispiel 2: Hinzufügen einer öffentlichen IP zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="4f29b-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="4f29b-116">Mit diesem Befehl wird ein Virtual Machine-Konfigurationsobjekt mithilfe des Cmdlets **New-AzureVMConfig** erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f29b-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="4f29b-117">Der Befehl übergibt das Objekt an das Cmdlet **Add-AzureProvisioningConfig** , das zusätzliche Konfiguration bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4f29b-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="4f29b-118">Das aktuelle Cmdlet fügt den öffentlichen IP-Namen ftpip hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f29b-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="4f29b-119">Der Befehl übergibt die Konfiguration an das Cmdlet **New-AzureVM** , das den virtuellen Computer erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f29b-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="4f29b-120">Beispiel 3: Hinzufügen einer öffentlichen IP-Adresse und einer Bezeichnung zu einem vorhandenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="4f29b-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="4f29b-121">Dieser Befehl ruft den virtuellen Computer mit dem Namen FTPInstance im Dienst FTPInAzure mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="4f29b-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="4f29b-122">Der Befehl übergibt diesen virtuellen Computer mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f29b-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4f29b-123">Das aktuelle Cmdlet addiert den öffentlichen IP-Namen ftpip und das Label ipname.</span><span class="sxs-lookup"><span data-stu-id="4f29b-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="4f29b-124">Der Befehl aktualisiert den virtuellen Computer, der Ihre Änderungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="4f29b-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="4f29b-125">Beispiel 4: Hinzufügen einer öffentlichen IP-Adresse und einer Bezeichnung zu einem neuen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="4f29b-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="4f29b-126">Mit diesem Befehl wird ein Virtual Machine Configuration-Objekt erstellt, und das Objekt wird dann an **Add-AzureProvisioningConfig** übergeben, wodurch eine zusätzliche Konfiguration bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f29b-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="4f29b-127">Das aktuelle Cmdlet addiert den öffentlichen IP-Namen ftpip und das Label ipname.</span><span class="sxs-lookup"><span data-stu-id="4f29b-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="4f29b-128">Der Befehl erstellt den virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="4f29b-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="4f29b-129">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f29b-129">PARAMETERS</span></span>

### <span data-ttu-id="4f29b-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="4f29b-130">-DomainNameLabel</span></span>
<span data-ttu-id="4f29b-131">Gibt den Namen an, der für einen entsprechenden DNS-Eintrag für die öffentliche IP-Adresse verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4f29b-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f29b-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="4f29b-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="4f29b-133">Gibt den TCP-Leerlauftimeout Zeitraum in Minuten an.</span><span class="sxs-lookup"><span data-stu-id="4f29b-133">Specifies the TCP idle time-out period in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f29b-134">-Information</span><span class="sxs-lookup"><span data-stu-id="4f29b-134">-InformationAction</span></span>
<span data-ttu-id="4f29b-135">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="4f29b-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4f29b-136">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4f29b-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4f29b-137">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="4f29b-137">Continue</span></span>
- <span data-ttu-id="4f29b-138">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="4f29b-138">Ignore</span></span>
- <span data-ttu-id="4f29b-139">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="4f29b-139">Inquire</span></span>
- <span data-ttu-id="4f29b-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4f29b-140">SilentlyContinue</span></span>
- <span data-ttu-id="4f29b-141">Beenden</span><span class="sxs-lookup"><span data-stu-id="4f29b-141">Stop</span></span>
- <span data-ttu-id="4f29b-142">Anhalten</span><span class="sxs-lookup"><span data-stu-id="4f29b-142">Suspend</span></span>

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

### <span data-ttu-id="4f29b-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4f29b-143">-InformationVariable</span></span>
<span data-ttu-id="4f29b-144">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="4f29b-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4f29b-145">-Profil</span><span class="sxs-lookup"><span data-stu-id="4f29b-145">-Profile</span></span>
<span data-ttu-id="4f29b-146">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4f29b-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f29b-147">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4f29b-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f29b-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="4f29b-148">-PublicIPName</span></span>
<span data-ttu-id="4f29b-149">Gibt den öffentlichen IP-Namen an.</span><span class="sxs-lookup"><span data-stu-id="4f29b-149">Specifies the Public IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f29b-150">-VM</span><span class="sxs-lookup"><span data-stu-id="4f29b-150">-VM</span></span>
<span data-ttu-id="4f29b-151">Gibt den virtuellen Computer an, dem dieses Cmdlet Public IP hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="4f29b-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f29b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f29b-152">CommonParameters</span></span>
<span data-ttu-id="4f29b-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f29b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f29b-154">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f29b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f29b-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f29b-155">INPUTS</span></span>

## <span data-ttu-id="4f29b-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f29b-156">OUTPUTS</span></span>

### <span data-ttu-id="4f29b-157">Microsoft. WindowsAzure. Commands. Servicemanagement. Model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="4f29b-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="4f29b-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f29b-158">NOTES</span></span>

## <span data-ttu-id="4f29b-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f29b-159">RELATED LINKS</span></span>

[<span data-ttu-id="4f29b-160">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="4f29b-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="4f29b-161">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4f29b-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="4f29b-162">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="4f29b-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="4f29b-163">Neu – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="4f29b-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="4f29b-164">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="4f29b-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="4f29b-165">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="4f29b-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


