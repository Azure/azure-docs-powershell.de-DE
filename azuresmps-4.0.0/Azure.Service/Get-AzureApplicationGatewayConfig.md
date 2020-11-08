---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A2F0ECAD-595C-45E6-98AC-2C7DB8E4BEF0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4dac85bf4c8b3d0a0f0f4b27cd249a98e020be7d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005871"
---
# <span data-ttu-id="9ded0-101">Get-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="9ded0-101">Get-AzureApplicationGatewayConfig</span></span>

## <span data-ttu-id="9ded0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ded0-102">SYNOPSIS</span></span>
<span data-ttu-id="9ded0-103">Ruft einen Anwendungs Gateway-Konfigurationskontext ab.</span><span class="sxs-lookup"><span data-stu-id="9ded0-103">Gets an Application Gateway configuration context.</span></span>

## <span data-ttu-id="9ded0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ded0-104">SYNTAX</span></span>

```
Get-AzureApplicationGatewayConfig -Name <String> [-ExportToFile <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ded0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ded0-105">DESCRIPTION</span></span>
<span data-ttu-id="9ded0-106">Das Cmdlet " **Get-AzureApplicationGatewayConfig** " Ruft einen Azure Application Gateway-Konfigurationskontext ab.</span><span class="sxs-lookup"><span data-stu-id="9ded0-106">The **Get-AzureApplicationGatewayConfig** cmdlet gets an Azure Application Gateway configuration context.</span></span>
<span data-ttu-id="9ded0-107">Ein Kontext umfasst sowohl ein Konfigurationsobjekt als auch eine XML-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9ded0-107">A context includes both a configuration object and XML configuration.</span></span>
<span data-ttu-id="9ded0-108">Sie können die XML-Konfiguration in einer Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="9ded0-108">You can save the XML configuration to a file.</span></span>

## <span data-ttu-id="9ded0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ded0-109">EXAMPLES</span></span>

### <span data-ttu-id="9ded0-110">Beispiel 1: Abrufen einer Application Gateway-Konfiguration und speichern in einer Datei</span><span class="sxs-lookup"><span data-stu-id="9ded0-110">Example 1: Get an Application Gateway configuration and save it to a file</span></span>
```
PS C:\> Get-AzureApplicationGatewayConfig -Name "ApplicationGateway06" -ExportToFile "D:\config.xml"
```

<span data-ttu-id="9ded0-111">Dieser Befehl ruft die Konfiguration für ein Anwendungs Gateway mit dem Namen ApplicationGateway06 ab.</span><span class="sxs-lookup"><span data-stu-id="9ded0-111">This command gets the configuration for an Application Gateway named ApplicationGateway06.</span></span>
<span data-ttu-id="9ded0-112">Der Befehl speichert ihn in der Datei im angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="9ded0-112">The command saves it in the file in the specified path.</span></span>

## <span data-ttu-id="9ded0-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ded0-113">PARAMETERS</span></span>

### <span data-ttu-id="9ded0-114">-ExportToFile</span><span class="sxs-lookup"><span data-stu-id="9ded0-114">-ExportToFile</span></span>
<span data-ttu-id="9ded0-115">Gibt einen Dateipfad an, zu dem dieses Cmdlet die Konfiguration im XML-Format speichert.</span><span class="sxs-lookup"><span data-stu-id="9ded0-115">Specifies a file path to which this cmdlet saves the configuration in XML format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ded0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9ded0-116">-Name</span></span>
<span data-ttu-id="9ded0-117">Gibt den Namen des Anwendungs Gateways an, für das dieses Cmdlet Konfigurationsinformationen erhält.</span><span class="sxs-lookup"><span data-stu-id="9ded0-117">Specifies the name of the Application Gateway for which this cmdlet gets configuration information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ded0-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="9ded0-118">-Profile</span></span>
<span data-ttu-id="9ded0-119">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9ded0-119">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="9ded0-120">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9ded0-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9ded0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ded0-121">CommonParameters</span></span>
<span data-ttu-id="9ded0-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ded0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ded0-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ded0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ded0-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ded0-124">INPUTS</span></span>

### <span data-ttu-id="9ded0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="9ded0-125">System.String</span></span>

## <span data-ttu-id="9ded0-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ded0-126">OUTPUTS</span></span>

### <span data-ttu-id="9ded0-127">Microsoft. Azure. Networking. ApplicationGatewayObjectModel. ApplicationGatewayConfigContext</span><span class="sxs-lookup"><span data-stu-id="9ded0-127">Microsoft.Azure.Networking.ApplicationGatewayObjectModel.ApplicationGatewayConfigContext</span></span>

## <span data-ttu-id="9ded0-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ded0-128">NOTES</span></span>

## <span data-ttu-id="9ded0-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ded0-129">RELATED LINKS</span></span>

[<span data-ttu-id="9ded0-130">Satz-AzureApplicationGatewayConfig</span><span class="sxs-lookup"><span data-stu-id="9ded0-130">Set-AzureApplicationGatewayConfig</span></span>](./Set-AzureApplicationGatewayConfig.md)


