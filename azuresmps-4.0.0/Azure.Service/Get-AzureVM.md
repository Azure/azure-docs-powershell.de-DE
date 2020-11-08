---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BBA0D5D3-29A5-4E00-9075-702E2F81CA52
online version: ''
schema: 2.0.0
ms.openlocfilehash: bcff7873042d9f7a07eee26f93312c8690e16416
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006753"
---
# <span data-ttu-id="ad11a-101">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad11a-101">Get-AzureVM</span></span>

## <span data-ttu-id="ad11a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad11a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad11a-103">Ruft Informationen von einem oder mehreren Azure Virtual Machines ab.</span><span class="sxs-lookup"><span data-stu-id="ad11a-103">Retrieves information from one or more Azure virtual machines.</span></span>

## <span data-ttu-id="ad11a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad11a-104">SYNTAX</span></span>

### <span data-ttu-id="ad11a-105">ListAllVMs (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad11a-105">ListAllVMs (Default)</span></span>
```
Get-AzureVM [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad11a-106">GetVMByServiceAndVMName</span><span class="sxs-lookup"><span data-stu-id="ad11a-106">GetVMByServiceAndVMName</span></span>
```
Get-AzureVM [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ad11a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad11a-107">DESCRIPTION</span></span>
<span data-ttu-id="ad11a-108">Das Cmdlet " **Get-AzureVM** " Ruft Informationen zu virtuellen Computern ab, die in Azure ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ad11a-108">The **Get-AzureVM** cmdlet retrieves information about virtual machines running in Azure.</span></span>
<span data-ttu-id="ad11a-109">Sie gibt ein Objekt mit Informationen auf einem bestimmten virtuellen Computer oder, wenn kein virtueller Computer angegeben ist, für alle virtuellen Computer im angegebenen Dienst des aktuellen Abonnements zurück.</span><span class="sxs-lookup"><span data-stu-id="ad11a-109">It returns an object with information on a specific virtual machine, or if no virtual machine is specified, for all the virtual machines in the specified service of the current subscription.</span></span>

## <span data-ttu-id="ad11a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad11a-110">EXAMPLES</span></span>

### <span data-ttu-id="ad11a-111">Beispiel 1: Abrufen von Informationen auf einem angegebenen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="ad11a-111">Example 1: Retrieve information on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "VirtualMachine02"
```

<span data-ttu-id="ad11a-112">Dieser Befehl gibt ein Objekt mit Informationen auf dem virtuellen VirtualMachine02-Computer zurück, der im ContosoService01-cloudbasierten Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ad11a-112">This command returns an object with information on the VirtualMachine02 virtual machine running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="ad11a-113">Beispiel 2: Abrufen von Informationen auf allen virtuellen Computern</span><span class="sxs-lookup"><span data-stu-id="ad11a-113">Example 2: Retrieve information on all virtual machines</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"
```

<span data-ttu-id="ad11a-114">Dieser Befehl ruft ein Listenobjekt mit Informationen zu allen virtuellen Computern ab, die im ContosoService01-clouddienst ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ad11a-114">This command retrieves a list object with information on all of the virtual machines running in the ContosoService01 cloud service.</span></span>

### <span data-ttu-id="ad11a-115">Beispiel 3: Anzeigen einer Tabelle mit den Status von virtuellen Computern</span><span class="sxs-lookup"><span data-stu-id="ad11a-115">Example 3: Display a table of virtual machine statuses</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01"  | Format-Table AutoSize -Property "Name",@{Expression={$_.InstanceUpgradeDomain};Label="UpgDom";Align="Right"},"InstanceStatus"
```

<span data-ttu-id="ad11a-116">Dieser Befehl zeigt eine Tabelle mit den virtuellen Computern, die im ContosoService01-Dienst ausgeführt werden, ihrer Upgrade-Domäne und dem aktuellen Status der einzelnen virtuellen Computer an.</span><span class="sxs-lookup"><span data-stu-id="ad11a-116">This command displays a table showing the virtual machines running on the ContosoService01 service, their Upgrade Domain, and the current status of each virtual machine.</span></span>

## <span data-ttu-id="ad11a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad11a-117">PARAMETERS</span></span>

### <span data-ttu-id="ad11a-118">-Information</span><span class="sxs-lookup"><span data-stu-id="ad11a-118">-InformationAction</span></span>
<span data-ttu-id="ad11a-119">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="ad11a-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ad11a-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ad11a-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ad11a-121">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="ad11a-121">Continue</span></span>
- <span data-ttu-id="ad11a-122">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="ad11a-122">Ignore</span></span>
- <span data-ttu-id="ad11a-123">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="ad11a-123">Inquire</span></span>
- <span data-ttu-id="ad11a-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ad11a-124">SilentlyContinue</span></span>
- <span data-ttu-id="ad11a-125">Beenden</span><span class="sxs-lookup"><span data-stu-id="ad11a-125">Stop</span></span>
- <span data-ttu-id="ad11a-126">Anhalten</span><span class="sxs-lookup"><span data-stu-id="ad11a-126">Suspend</span></span>

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

### <span data-ttu-id="ad11a-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ad11a-127">-InformationVariable</span></span>
<span data-ttu-id="ad11a-128">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="ad11a-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ad11a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="ad11a-129">-Name</span></span>
<span data-ttu-id="ad11a-130">Gibt den Namen des virtuellen Computers an, für den Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ad11a-130">Specifies the name of the virtual machine for which to retrieve information.</span></span>
<span data-ttu-id="ad11a-131">Wenn dieser Parameter nicht angegeben wird, gibt das Cmdlet ein Listenobjekt mit Informationen zu allen virtuellen Computern im angegebenen Dienst zurück.</span><span class="sxs-lookup"><span data-stu-id="ad11a-131">If this parameter is not provided, the cmdlet returns a list object with information about all the virtual machines in the specified service.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad11a-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="ad11a-132">-Profile</span></span>
<span data-ttu-id="ad11a-133">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ad11a-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ad11a-134">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ad11a-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ad11a-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ad11a-135">-ServiceName</span></span>
<span data-ttu-id="ad11a-136">Gibt den Namen des Cloud-Diensts an, für den Informationen zu virtuellen Maschinen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ad11a-136">Specifies the name of the cloud service for which to return virtual machine information.</span></span>

```yaml
Type: String
Parameter Sets: GetVMByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad11a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad11a-137">CommonParameters</span></span>
<span data-ttu-id="ad11a-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad11a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad11a-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad11a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad11a-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad11a-140">INPUTS</span></span>

## <span data-ttu-id="ad11a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad11a-141">OUTPUTS</span></span>

## <span data-ttu-id="ad11a-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad11a-142">NOTES</span></span>

## <span data-ttu-id="ad11a-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad11a-143">RELATED LINKS</span></span>

[<span data-ttu-id="ad11a-144">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad11a-144">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ad11a-145">Neu – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ad11a-145">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ad11a-146">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad11a-146">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="ad11a-147">Neustart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad11a-147">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="ad11a-148">Anfang-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad11a-148">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="ad11a-149">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad11a-149">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="ad11a-150">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ad11a-150">Update-AzureVM</span></span>](./Update-AzureVM.md)


