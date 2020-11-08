---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5A068EC9-3745-4219-BA03-C56CB9D9D157
online version: ''
schema: 2.0.0
ms.openlocfilehash: 24fad9fc499c3f7abec5e7539fd1e221835849ce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006684"
---
# <span data-ttu-id="d7a06-101">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7a06-101">Remove-AzureEndpoint</span></span>

## <span data-ttu-id="d7a06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7a06-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a06-103">Löscht einen Endpunkt von einem virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="d7a06-103">Deletes an endpoint from an Azure virtual machine.</span></span>

## <span data-ttu-id="d7a06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7a06-104">SYNTAX</span></span>

```
Remove-AzureEndpoint [-Name] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d7a06-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7a06-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a06-106">Das Cmdlet **Remove-AzureEndpoint** löscht einen Endpunkt aus einem Azure Virtual Machine-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7a06-106">The **Remove-AzureEndpoint** cmdlet deletes an endpoint from an Azure virtual machine object.</span></span>

## <span data-ttu-id="d7a06-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7a06-107">EXAMPLES</span></span>

### <span data-ttu-id="d7a06-108">Beispiel 1: Entfernen eines Endpunkts</span><span class="sxs-lookup"><span data-stu-id="d7a06-108">Example 1: Remove an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine01" | Remove-AzureEndpoint -Name "HttpIn" | Update-AzureVM
```

<span data-ttu-id="d7a06-109">Dieser Befehl ruft mit dem Cmdlet **Get-AzureVM** die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine01 ab.</span><span class="sxs-lookup"><span data-stu-id="d7a06-109">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="d7a06-110">Der Befehl übergibt ihn mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7a06-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d7a06-111">Dieses Cmdlet entfernt einen Endpunkt mit dem Namen httpin.</span><span class="sxs-lookup"><span data-stu-id="d7a06-111">This cmdlet removes an endpoint named HttpIn.</span></span>
<span data-ttu-id="d7a06-112">Der Befehl übergibt das Objekt des virtuellen Computers an das Cmdlet **Update-AzureVM** , das Ihre Änderungen implementiert.</span><span class="sxs-lookup"><span data-stu-id="d7a06-112">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

## <span data-ttu-id="d7a06-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7a06-113">PARAMETERS</span></span>

### <span data-ttu-id="d7a06-114">-Information</span><span class="sxs-lookup"><span data-stu-id="d7a06-114">-InformationAction</span></span>
<span data-ttu-id="d7a06-115">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="d7a06-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d7a06-116">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d7a06-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d7a06-117">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="d7a06-117">Continue</span></span>
- <span data-ttu-id="d7a06-118">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d7a06-118">Ignore</span></span>
- <span data-ttu-id="d7a06-119">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="d7a06-119">Inquire</span></span>
- <span data-ttu-id="d7a06-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d7a06-120">SilentlyContinue</span></span>
- <span data-ttu-id="d7a06-121">Beenden</span><span class="sxs-lookup"><span data-stu-id="d7a06-121">Stop</span></span>
- <span data-ttu-id="d7a06-122">Anhalten</span><span class="sxs-lookup"><span data-stu-id="d7a06-122">Suspend</span></span>

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

### <span data-ttu-id="d7a06-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d7a06-123">-InformationVariable</span></span>
<span data-ttu-id="d7a06-124">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="d7a06-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d7a06-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d7a06-125">-Name</span></span>
<span data-ttu-id="d7a06-126">Gibt den Namen des Endpunkts an, den dieses Cmdlet vom virtuellen Computer löscht.</span><span class="sxs-lookup"><span data-stu-id="d7a06-126">Specifies the name of the endpoint that this cmdlet deletes from the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7a06-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="d7a06-127">-Profile</span></span>
<span data-ttu-id="d7a06-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d7a06-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d7a06-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d7a06-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d7a06-130">-VM</span><span class="sxs-lookup"><span data-stu-id="d7a06-130">-VM</span></span>
<span data-ttu-id="d7a06-131">Gibt den virtuellen Computer an, von dem dieses Cmdlet einen Endpunkt löscht.</span><span class="sxs-lookup"><span data-stu-id="d7a06-131">Specifies the virtual machine from which this cmdlet deletes an endpoint.</span></span>

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

### <span data-ttu-id="d7a06-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a06-132">CommonParameters</span></span>
<span data-ttu-id="d7a06-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7a06-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a06-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a06-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a06-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7a06-135">INPUTS</span></span>

## <span data-ttu-id="d7a06-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7a06-136">OUTPUTS</span></span>

## <span data-ttu-id="d7a06-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7a06-137">NOTES</span></span>

## <span data-ttu-id="d7a06-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7a06-138">RELATED LINKS</span></span>

[<span data-ttu-id="d7a06-139">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7a06-139">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="d7a06-140">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7a06-140">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="d7a06-141">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d7a06-141">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="d7a06-142">Satz-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="d7a06-142">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="d7a06-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d7a06-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


