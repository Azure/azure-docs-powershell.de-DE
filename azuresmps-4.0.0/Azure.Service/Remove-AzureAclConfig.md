---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 915CBA29-5A58-4A5D-9F02-976CB76D4800
online version: ''
schema: 2.0.0
ms.openlocfilehash: af98cbdc0be73c87682d0ed004d17cd9e82c9baa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006381"
---
# <span data-ttu-id="a54cb-101">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a54cb-101">Remove-AzureAclConfig</span></span>

## <span data-ttu-id="a54cb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a54cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a54cb-103">Entfernt ein ACL-Konfigurationsobjekt aus einer Azure Virtual Machine-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a54cb-103">Removes an ACL configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="a54cb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a54cb-104">SYNTAX</span></span>

```
Remove-AzureAclConfig [-EndpointName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a54cb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a54cb-105">DESCRIPTION</span></span>
<span data-ttu-id="a54cb-106">Das Cmdlet **Remove-AzureAclConfig** entfernt ein Configuration-Objekt für die Zugriffssteuerungsliste (ACL) aus einer Azure Virtual Machine-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a54cb-106">The **Remove-AzureAclConfig** cmdlet removes an access control list (ACL) configuration object from an Azure virtual machine configuration.</span></span>

## <span data-ttu-id="a54cb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a54cb-107">EXAMPLES</span></span>

### <span data-ttu-id="a54cb-108">Beispiel 1: Entfernen einer ACL-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a54cb-108">Example 1: Remove an ACL configuration</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureAclConfig -EndpointName "Web" | Update-AzureVM
```

<span data-ttu-id="a54cb-109">Dieser Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="a54cb-109">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a54cb-110">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a54cb-110">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a54cb-111">Dieses Cmdlet entfernt die ACL-Konfiguration für den Endpunkt mit dem Namen Web.</span><span class="sxs-lookup"><span data-stu-id="a54cb-111">That cmdlet removes the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="a54cb-112">Der Befehl übergibt das Ergebnis an das Cmdlet **Update-AzureVM** , das den virtuellen Computer aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a54cb-112">The command passes the result to the **Update-AzureVM** cmdlet, which updates the virtual machine.</span></span>

## <span data-ttu-id="a54cb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a54cb-113">PARAMETERS</span></span>

### <span data-ttu-id="a54cb-114">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="a54cb-114">-EndpointName</span></span>
<span data-ttu-id="a54cb-115">Gibt den Namen des Endpunkts an, von dem dieses Cmdlet die ACL-Konfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="a54cb-115">Specifies the name of the endpoint from which this cmdlet removes the ACL configuration.</span></span>

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

### <span data-ttu-id="a54cb-116">-Information</span><span class="sxs-lookup"><span data-stu-id="a54cb-116">-InformationAction</span></span>
<span data-ttu-id="a54cb-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="a54cb-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a54cb-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a54cb-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a54cb-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="a54cb-119">Continue</span></span>
- <span data-ttu-id="a54cb-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a54cb-120">Ignore</span></span>
- <span data-ttu-id="a54cb-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="a54cb-121">Inquire</span></span>
- <span data-ttu-id="a54cb-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a54cb-122">SilentlyContinue</span></span>
- <span data-ttu-id="a54cb-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="a54cb-123">Stop</span></span>
- <span data-ttu-id="a54cb-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="a54cb-124">Suspend</span></span>

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

### <span data-ttu-id="a54cb-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a54cb-125">-InformationVariable</span></span>
<span data-ttu-id="a54cb-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="a54cb-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a54cb-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="a54cb-127">-Profile</span></span>
<span data-ttu-id="a54cb-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a54cb-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a54cb-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a54cb-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a54cb-130">-VM</span><span class="sxs-lookup"><span data-stu-id="a54cb-130">-VM</span></span>
<span data-ttu-id="a54cb-131">Gibt den virtuellen Computer an, von dem dieses Cmdlet eine ACL-Konfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="a54cb-131">Specifies the virtual machine from which this cmdlet removes an ACL configuration.</span></span>

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

### <span data-ttu-id="a54cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a54cb-132">CommonParameters</span></span>
<span data-ttu-id="a54cb-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a54cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a54cb-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a54cb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a54cb-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a54cb-135">INPUTS</span></span>

## <span data-ttu-id="a54cb-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a54cb-136">OUTPUTS</span></span>

## <span data-ttu-id="a54cb-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a54cb-137">NOTES</span></span>

## <span data-ttu-id="a54cb-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a54cb-138">RELATED LINKS</span></span>

[<span data-ttu-id="a54cb-139">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a54cb-139">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="a54cb-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a54cb-140">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a54cb-141">Neu – AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a54cb-141">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="a54cb-142">Satz-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a54cb-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)

[<span data-ttu-id="a54cb-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a54cb-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


