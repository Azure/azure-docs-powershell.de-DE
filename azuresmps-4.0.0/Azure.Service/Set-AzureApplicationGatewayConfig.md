---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D7D99AFA-A85E-43DA-9F2F-8FFD34048E00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ede675ab58905f102fb9d0029669115acdb9e85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006635"
---
# <span data-ttu-id="99d95-101">Set-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="99d95-101">Set-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="99d95-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="99d95-102">SYNOPSIS</span></span>
<span data-ttu-id="99d95-103">Konfiguriert ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="99d95-103">Configures an application gateway.</span></span>

## <span data-ttu-id="99d95-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="99d95-104">SYNTAX</span></span>

### <span data-ttu-id="99d95-105">configFile</span><span class="sxs-lookup"><span data-stu-id="99d95-105">configFile</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -ConfigFile <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="99d95-106">configobject</span><span class="sxs-lookup"><span data-stu-id="99d95-106">configObject</span></span>
```
Set-AzureApplicationGatewayConfig -Name <String> -Config <ApplicationGatewayConfiguration>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="99d95-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="99d95-107">DESCRIPTION</span></span>
<span data-ttu-id="99d95-108">Das Cmdlet " **Satz-AzureApplicationGatewayConfig** " konfiguriert ein Anwendungsgateway.</span><span class="sxs-lookup"><span data-stu-id="99d95-108">The **Set-AzureApplicationGatewayConfig** cmdlet configures an application gateway.</span></span>

## <span data-ttu-id="99d95-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="99d95-109">EXAMPLES</span></span>

### <span data-ttu-id="99d95-110">Beispiel 1: Konfigurieren eines Anwendungs Gateways mithilfe eines Configuration-Objekts</span><span class="sxs-lookup"><span data-stu-id="99d95-110">Example 1: Configure an application gateway by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway02"
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -Config $ConfigReturnObject
```

<span data-ttu-id="99d95-111">Der erste Befehl ruft das Konfigurationsobjekt für das Anwendungsgateway mit dem Namen ApplicationGateway02 mit dem Cmdlet **Get-AzureApplicationGatewayConfig** ab.</span><span class="sxs-lookup"><span data-stu-id="99d95-111">The first command gets the configuration object for the application gateway named ApplicationGateway02 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="99d95-112">Der Befehl speichert Sie in der $ConfigReturnObject-Variablen.</span><span class="sxs-lookup"><span data-stu-id="99d95-112">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="99d95-113">Der zweite Befehl legt die Konfiguration für die Anwendung mit dem Namen ApplicationGateway06 mithilfe eines in der $ConfigReturnObject Variablen gespeicherten Application Gateway-Konfigurationsobjekts fest.</span><span class="sxs-lookup"><span data-stu-id="99d95-113">The second command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration object stored in the $ConfigReturnObject variable.</span></span>

### <span data-ttu-id="99d95-114">Beispiel 2: Konfigurieren eines Anwendungs Gateways mithilfe einer Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="99d95-114">Example 2: Configure an application gateway by using a configuration file</span></span>
```
PS C:\> Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ConfigFile "D:\config.xml"
```

<span data-ttu-id="99d95-115">Mit diesem Befehl wird die Konfiguration für die Anwendung mit dem Namen ApplicationGateway06 unter Verwendung einer Application Gateway-Konfigurationsdatei am angegebenen Speicherort festgelegt.</span><span class="sxs-lookup"><span data-stu-id="99d95-115">This command sets the configuration for the application named ApplicationGateway06 by using an application gateway configuration file in the specified location.</span></span>

### <span data-ttu-id="99d95-116">Beispiel 3: Ändern einer Konfiguration mithilfe eines Configuration-Objekts</span><span class="sxs-lookup"><span data-stu-id="99d95-116">Example 3: Modify a configuration by using a configuration object</span></span>
```
PS C:\> $ConfigReturnObject = Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
PS C:\> $ConfigReturnObject.Config.FrontendPorts[0].Port = 443
PS C:\> $ConfigReturnObject | Set-AzureApplicationGatewayConfig -Name "ApplicationGateway06"
```

<span data-ttu-id="99d95-117">Der erste Befehl ruft das Konfigurationsobjekt für das Anwendungsgateway mit dem Namen ApplicationGateway06 mit dem Cmdlet **Get-AzureApplicationGatewayConfig** ab.</span><span class="sxs-lookup"><span data-stu-id="99d95-117">The first command gets the configuration object for the application gateway named ApplicationGateway06 by using the **Get-AzureApplicationGatewayConfig** cmdlet.</span></span>
<span data-ttu-id="99d95-118">Der Befehl speichert Sie in der $ConfigReturnObject-Variablen.</span><span class="sxs-lookup"><span data-stu-id="99d95-118">The command stores it in the $ConfigReturnObject variable.</span></span>

<span data-ttu-id="99d95-119">Der zweite Befehl weist einer **Port** -Eigenschaft in dem in $ConfigReturnObject gespeicherten Objekt einen Port Wert zu.</span><span class="sxs-lookup"><span data-stu-id="99d95-119">The second command assigns a port value to a **Port** property in the object stored in $ConfigReturnObject.</span></span>

<span data-ttu-id="99d95-120">Der letzte Befehl übergibt den aktualisierten $ConfigReturnObject an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99d95-120">The final command passes the updated $ConfigReturnObject to the current cmdlet.</span></span>

## <span data-ttu-id="99d95-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="99d95-121">PARAMETERS</span></span>

### <span data-ttu-id="99d95-122">-Config</span><span class="sxs-lookup"><span data-stu-id="99d95-122">-Config</span></span>
<span data-ttu-id="99d95-123">Gibt ein Configuration-Objekt für das Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="99d95-123">Specifies an application gateway configuration object.</span></span>
<span data-ttu-id="99d95-124">Dieses Cmdlet weist die Konfiguration zu, die dieser Parameter einem Anwendungsgateway angibt.</span><span class="sxs-lookup"><span data-stu-id="99d95-124">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: ApplicationGatewayConfiguration
Parameter Sets: configObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d95-125">-Configdatei</span><span class="sxs-lookup"><span data-stu-id="99d95-125">-ConfigFile</span></span>
<span data-ttu-id="99d95-126">Gibt den Pfad einer Konfigurationsdatei im XML-Format für ein Anwendungsgateway an.</span><span class="sxs-lookup"><span data-stu-id="99d95-126">Specifies the path of a configuration file, in XML format, for an application gateway.</span></span>
<span data-ttu-id="99d95-127">Dieses Cmdlet weist die Konfiguration zu, die dieser Parameter einem Anwendungsgateway angibt.</span><span class="sxs-lookup"><span data-stu-id="99d95-127">This cmdlet assigns the configuration that this parameter specifies to an application gateway.</span></span>

```yaml
Type: String
Parameter Sets: configFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99d95-128">-Name</span><span class="sxs-lookup"><span data-stu-id="99d95-128">-Name</span></span>
<span data-ttu-id="99d95-129">Gibt den Namen des Anwendungs Gateways an, das von diesem Cmdlet konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="99d95-129">Specifies the name of the application gateway that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99d95-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="99d95-130">-Profile</span></span>
<span data-ttu-id="99d95-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="99d95-131">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="99d95-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="99d95-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="99d95-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99d95-133">CommonParameters</span></span>
<span data-ttu-id="99d95-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99d95-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99d95-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99d95-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99d95-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="99d95-136">INPUTS</span></span>

### <span data-ttu-id="99d95-137">System. String, Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfiguration</span><span class="sxs-lookup"><span data-stu-id="99d95-137">System.String, Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfiguration</span></span>

## <span data-ttu-id="99d95-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="99d95-138">OUTPUTS</span></span>

### <span data-ttu-id="99d95-139">Microsoft. WindowsAzure. Management. ApplicationGateway. Models. ApplicationGatewayOperationResponse</span><span class="sxs-lookup"><span data-stu-id="99d95-139">Microsoft.WindowsAzure.Management.ApplicationGateway.Models.ApplicationGatewayOperationResponse</span></span>

## <span data-ttu-id="99d95-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="99d95-140">NOTES</span></span>

## <span data-ttu-id="99d95-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="99d95-141">RELATED LINKS</span></span>

[<span data-ttu-id="99d95-142">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="99d95-142">Get-AzureApplicationGatewayConfig</span></span>](./Get-AzureApplicationGatewayConfig.md)


