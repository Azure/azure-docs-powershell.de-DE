---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005812"
---
# <span data-ttu-id="66178-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="66178-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="66178-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66178-102">SYNOPSIS</span></span>
<span data-ttu-id="66178-103">Ruft Informationen zu den verfügbaren Erweiterungen für gehostete Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="66178-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="66178-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66178-104">SYNTAX</span></span>

### <span data-ttu-id="66178-105">ListLatestExtensions (Standard)</span><span class="sxs-lookup"><span data-stu-id="66178-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="66178-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="66178-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="66178-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="66178-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="66178-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66178-108">DESCRIPTION</span></span>
<span data-ttu-id="66178-109">Das Cmdlet " **Get-AzureServiceAvailableExtension** " Ruft Informationen zu den neuesten verfügbaren Erweiterungen für gehostete Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="66178-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="66178-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66178-110">EXAMPLES</span></span>

### <span data-ttu-id="66178-111">Beispiel 1: Abrufen verfügbarer Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="66178-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="66178-112">Dieser Befehl ruft alle verfügbaren Erweiterungen ab.</span><span class="sxs-lookup"><span data-stu-id="66178-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="66178-113">Beispiel 2: Abrufen von Erweiterungen in einem angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="66178-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="66178-114">Dieser Befehl ruft die Erweiterungen mit einem angegebenen Namen in einem angegebenen Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="66178-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="66178-115">Beispiel 3: Abrufen einer bestimmten Version einer Erweiterung</span><span class="sxs-lookup"><span data-stu-id="66178-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="66178-116">Dieser Befehl ruft Informationen zu einer bestimmten Version einer Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="66178-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="66178-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="66178-117">PARAMETERS</span></span>

### <span data-ttu-id="66178-118">-Allversions</span><span class="sxs-lookup"><span data-stu-id="66178-118">-AllVersions</span></span>
<span data-ttu-id="66178-119">Gibt an, dass dieses Cmdlet alle Versionen einer Erweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="66178-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66178-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="66178-120">-ExtensionName</span></span>
<span data-ttu-id="66178-121">Gibt den Namen der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="66178-121">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66178-122">-Information</span><span class="sxs-lookup"><span data-stu-id="66178-122">-InformationAction</span></span>
<span data-ttu-id="66178-123">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="66178-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="66178-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="66178-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66178-125">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="66178-125">Continue</span></span>
- <span data-ttu-id="66178-126">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="66178-126">Ignore</span></span>
- <span data-ttu-id="66178-127">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="66178-127">Inquire</span></span>
- <span data-ttu-id="66178-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="66178-128">SilentlyContinue</span></span>
- <span data-ttu-id="66178-129">Beenden</span><span class="sxs-lookup"><span data-stu-id="66178-129">Stop</span></span>
- <span data-ttu-id="66178-130">Anhalten</span><span class="sxs-lookup"><span data-stu-id="66178-130">Suspend</span></span>

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

### <span data-ttu-id="66178-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="66178-131">-InformationVariable</span></span>
<span data-ttu-id="66178-132">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="66178-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="66178-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="66178-133">-Profile</span></span>
<span data-ttu-id="66178-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="66178-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66178-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="66178-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66178-136">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="66178-136">-ProviderNamespace</span></span>
<span data-ttu-id="66178-137">Gibt den Namespace des Erweiterungs Anbieters an.</span><span class="sxs-lookup"><span data-stu-id="66178-137">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66178-138">-Version</span><span class="sxs-lookup"><span data-stu-id="66178-138">-Version</span></span>
<span data-ttu-id="66178-139">Gibt die Erweiterungsversion an.</span><span class="sxs-lookup"><span data-stu-id="66178-139">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66178-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66178-140">CommonParameters</span></span>
<span data-ttu-id="66178-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66178-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66178-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66178-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66178-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66178-143">INPUTS</span></span>

## <span data-ttu-id="66178-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66178-144">OUTPUTS</span></span>

## <span data-ttu-id="66178-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="66178-145">NOTES</span></span>

## <span data-ttu-id="66178-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66178-146">RELATED LINKS</span></span>

[<span data-ttu-id="66178-147">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="66178-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)


