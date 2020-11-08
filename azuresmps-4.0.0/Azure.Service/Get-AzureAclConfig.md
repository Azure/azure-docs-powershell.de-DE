---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0A32348E-C38D-4555-8F7C-6515F4EE7F23
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc1c469d35f4cc281fa22252e7e81509be06761
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005879"
---
# <span data-ttu-id="a40a6-101">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a40a6-101">Get-AzureAclConfig</span></span>

## <span data-ttu-id="a40a6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a40a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a40a6-103">Ruft das ACL-Konfigurationsobjekt von einem Azure Virtual Machine ab.</span><span class="sxs-lookup"><span data-stu-id="a40a6-103">Gets the ACL configuration object from an Azure virtual machine.</span></span>

## <span data-ttu-id="a40a6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a40a6-104">SYNTAX</span></span>

```
Get-AzureAclConfig [[-EndpointName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a40a6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a40a6-105">DESCRIPTION</span></span>
<span data-ttu-id="a40a6-106">Das Cmdlet " **Get-AzureAclConfig** " Ruft das Konfigurationsobjekt für die Zugriffssteuerungsliste (ACL) von einem vorhandenen Azure Virtual Machine ab.</span><span class="sxs-lookup"><span data-stu-id="a40a6-106">The **Get-AzureAclConfig** cmdlet gets the access control list (ACL) configuration object from an existing Azure virtual machine.</span></span>

## <span data-ttu-id="a40a6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a40a6-107">EXAMPLES</span></span>

### <span data-ttu-id="a40a6-108">Beispiel 1: Abrufen eines ACL-Konfigurationsobjekts für einen Endpunkt einer virtuellen Maschine</span><span class="sxs-lookup"><span data-stu-id="a40a6-108">Example 1: Get an ACL configuration object for a virtual machine endpoint</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
```

<span data-ttu-id="a40a6-109">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="a40a6-109">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="a40a6-110">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das Cmdlet " **Get-AzureAclConfig** ".</span><span class="sxs-lookup"><span data-stu-id="a40a6-110">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a40a6-111">Dieses Cmdlet ruft die ACL-Konfiguration für den Endpunkt mit dem Namen Web ab.</span><span class="sxs-lookup"><span data-stu-id="a40a6-111">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="a40a6-112">Der Befehl speichert das ACL-Konfigurationsobjekt in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a40a6-112">The command stores that ACL configuration object in the $Acl variable.</span></span>

## <span data-ttu-id="a40a6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a40a6-113">PARAMETERS</span></span>

### <span data-ttu-id="a40a6-114">-Endpunktname</span><span class="sxs-lookup"><span data-stu-id="a40a6-114">-EndpointName</span></span>
<span data-ttu-id="a40a6-115">Gibt den Namen des Endpunkts an, für den dieses Cmdlet eine ACL erhält.</span><span class="sxs-lookup"><span data-stu-id="a40a6-115">Specifies the name of the endpoint for which this cmdlet gets an ACL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a40a6-116">-Information</span><span class="sxs-lookup"><span data-stu-id="a40a6-116">-InformationAction</span></span>
<span data-ttu-id="a40a6-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="a40a6-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a40a6-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a40a6-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a40a6-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="a40a6-119">Continue</span></span>
- <span data-ttu-id="a40a6-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a40a6-120">Ignore</span></span>
- <span data-ttu-id="a40a6-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="a40a6-121">Inquire</span></span>
- <span data-ttu-id="a40a6-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a40a6-122">SilentlyContinue</span></span>
- <span data-ttu-id="a40a6-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="a40a6-123">Stop</span></span>
- <span data-ttu-id="a40a6-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="a40a6-124">Suspend</span></span>

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

### <span data-ttu-id="a40a6-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a40a6-125">-InformationVariable</span></span>
<span data-ttu-id="a40a6-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="a40a6-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a40a6-127">-Profil</span><span class="sxs-lookup"><span data-stu-id="a40a6-127">-Profile</span></span>
<span data-ttu-id="a40a6-128">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a40a6-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a40a6-129">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a40a6-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a40a6-130">-VM</span><span class="sxs-lookup"><span data-stu-id="a40a6-130">-VM</span></span>
<span data-ttu-id="a40a6-131">Gibt das Objekt des virtuellen Computers an, für das dieses Cmdlet eine ACL-Konfiguration erhält.</span><span class="sxs-lookup"><span data-stu-id="a40a6-131">Specifies the virtual machine object for which this cmdlet gets ACL configuration.</span></span>

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

### <span data-ttu-id="a40a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a40a6-132">CommonParameters</span></span>
<span data-ttu-id="a40a6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a40a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a40a6-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a40a6-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a40a6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a40a6-135">INPUTS</span></span>

## <span data-ttu-id="a40a6-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a40a6-136">OUTPUTS</span></span>

## <span data-ttu-id="a40a6-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="a40a6-137">NOTES</span></span>

## <span data-ttu-id="a40a6-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a40a6-138">RELATED LINKS</span></span>

[<span data-ttu-id="a40a6-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a40a6-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a40a6-140">Neu – AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a40a6-140">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="a40a6-141">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a40a6-141">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="a40a6-142">Satz-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="a40a6-142">Set-AzureAclConfig</span></span>](./Set-AzureAclConfig.md)


