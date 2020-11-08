---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 184FB33A-C866-4AF0-BA31-8ADCFC6EE8E2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 15ce5d8511383ad93e288b97381416d7864c3f80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005852"
---
# <span data-ttu-id="b3943-101">Get-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b3943-101">Get-AzureDns</span></span>

## <span data-ttu-id="b3943-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3943-102">SYNOPSIS</span></span>
<span data-ttu-id="b3943-103">Ruft die DNS-Einstellungen für eine Azure-Bereitstellung ab.</span><span class="sxs-lookup"><span data-stu-id="b3943-103">Gets the DNS settings for an Azure deployment.</span></span>

## <span data-ttu-id="b3943-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3943-104">SYNTAX</span></span>

```
Get-AzureDns [-DnsSettings <DnsSettings>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b3943-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3943-105">DESCRIPTION</span></span>
<span data-ttu-id="b3943-106">Das Cmdlet " **Get-AzureDns** " Ruft die DNS-Einstellungen für eine Azure-Bereitstellung ab.</span><span class="sxs-lookup"><span data-stu-id="b3943-106">The **Get-AzureDns** cmdlet gets the DNS settings for an Azure deployment.</span></span>
<span data-ttu-id="b3943-107">Das Cmdlet gibt den Anzeigenamen und die IP-Adresse des DNS-Servers in einem DNS-Einstellungsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b3943-107">The cmdlet returns the friendly name and IP address of the DNS server in a DNS settings object.</span></span>

## <span data-ttu-id="b3943-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3943-108">EXAMPLES</span></span>

### <span data-ttu-id="b3943-109">Beispiel 1: Abrufen von DNS-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b3943-109">Example 1: Get DNS settings</span></span>
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Production" | Get-AzureDNS
```

<span data-ttu-id="b3943-110">Dieser Befehl verwendet das Cmdlet " **Get-AzureDeployment** ", um die Produktionsbereitstellung des Diensts mit dem Namen ContosoService zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b3943-110">This command uses the **Get-AzureDeployment** cmdlet to get the production deployment of the service named ContosoService.</span></span>
<span data-ttu-id="b3943-111">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3943-111">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b3943-112">Das aktuelle Cmdlet ruft die DNS-Einstellungen ab.</span><span class="sxs-lookup"><span data-stu-id="b3943-112">The current cmdlet gets the DNS settings.</span></span>

## <span data-ttu-id="b3943-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3943-113">PARAMETERS</span></span>

### <span data-ttu-id="b3943-114">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="b3943-114">-DnsSettings</span></span>
<span data-ttu-id="b3943-115">Gibt ein **DnsSettings** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="b3943-115">Specifies a **DnsSettings** object.</span></span>

```yaml
Type: DnsSettings
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3943-116">-Information</span><span class="sxs-lookup"><span data-stu-id="b3943-116">-InformationAction</span></span>
<span data-ttu-id="b3943-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="b3943-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b3943-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b3943-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b3943-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="b3943-119">Continue</span></span>
- <span data-ttu-id="b3943-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="b3943-120">Ignore</span></span>
- <span data-ttu-id="b3943-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="b3943-121">Inquire</span></span>
- <span data-ttu-id="b3943-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b3943-122">SilentlyContinue</span></span>
- <span data-ttu-id="b3943-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="b3943-123">Stop</span></span>
- <span data-ttu-id="b3943-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="b3943-124">Suspend</span></span>

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

### <span data-ttu-id="b3943-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b3943-125">-InformationVariable</span></span>
<span data-ttu-id="b3943-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="b3943-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b3943-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3943-127">CommonParameters</span></span>
<span data-ttu-id="b3943-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3943-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3943-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3943-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3943-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3943-130">INPUTS</span></span>

## <span data-ttu-id="b3943-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3943-131">OUTPUTS</span></span>

## <span data-ttu-id="b3943-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3943-132">NOTES</span></span>

## <span data-ttu-id="b3943-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3943-133">RELATED LINKS</span></span>

[<span data-ttu-id="b3943-134">Add-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b3943-134">Add-AzureDns</span></span>](./Add-AzureDns.md)

[<span data-ttu-id="b3943-135">Get-AzureDeployment</span><span class="sxs-lookup"><span data-stu-id="b3943-135">Get-AzureDeployment</span></span>](./Get-AzureDeployment.md)

[<span data-ttu-id="b3943-136">Neu – AzureDns</span><span class="sxs-lookup"><span data-stu-id="b3943-136">New-AzureDns</span></span>](./New-AzureDns.md)

[<span data-ttu-id="b3943-137">Remove-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b3943-137">Remove-AzureDns</span></span>](./Remove-AzureDns.md)

[<span data-ttu-id="b3943-138">Satz-AzureDns</span><span class="sxs-lookup"><span data-stu-id="b3943-138">Set-AzureDns</span></span>](./Set-AzureDns.md)


