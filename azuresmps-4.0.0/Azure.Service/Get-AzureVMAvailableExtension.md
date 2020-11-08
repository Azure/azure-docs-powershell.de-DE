---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006750"
---
# <span data-ttu-id="d09c6-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="d09c6-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="d09c6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d09c6-102">SYNOPSIS</span></span>
<span data-ttu-id="d09c6-103">Ruft Informationen zu den neuesten verfügbaren Erweiterungen für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="d09c6-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="d09c6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d09c6-104">SYNTAX</span></span>

### <span data-ttu-id="d09c6-105">ListLatestExtensions (Standard)</span><span class="sxs-lookup"><span data-stu-id="d09c6-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d09c6-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="d09c6-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d09c6-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="d09c6-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d09c6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d09c6-108">DESCRIPTION</span></span>
<span data-ttu-id="d09c6-109">Das Cmdlet " **Get-AzureVMAvailableExtension** " Ruft Informationen zu den neuesten verfügbaren Erweiterungen für virtuelle Computer ab.</span><span class="sxs-lookup"><span data-stu-id="d09c6-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="d09c6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d09c6-110">EXAMPLES</span></span>

### <span data-ttu-id="d09c6-111">Beispiel 1: Abrufen von Informationen zu den neuesten verfügbaren Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="d09c6-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="d09c6-112">Dieser Befehl ruft Informationen zu den neuesten verfügbaren Erweiterungen für alle virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="d09c6-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="d09c6-113">Beispiel 2: Abrufen von Informationen aus einem angegebenen Erweiterungsnamen</span><span class="sxs-lookup"><span data-stu-id="d09c6-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="d09c6-114">Dieser Befehl ruft Informationen aus allen Versionen der Erweiterung mit dem Namen VMAccessAgent und dem Herausgeber mit dem Namen Microsoft. Computer ab.</span><span class="sxs-lookup"><span data-stu-id="d09c6-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="d09c6-115">Beispiel 3: Abrufen von Informationen aus einer bestimmten virtuellen Computererweiterung nach Versionsnummer</span><span class="sxs-lookup"><span data-stu-id="d09c6-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="d09c6-116">Dieser Befehl ruft Informationen für die Erweiterung mit dem Namen VMAccessAgent und den Herausgeber mit dem Namen Microsoft. Compute für die Erweiterung Version 1.0.3 ab.</span><span class="sxs-lookup"><span data-stu-id="d09c6-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="d09c6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="d09c6-117">PARAMETERS</span></span>

### <span data-ttu-id="d09c6-118">-Allversions</span><span class="sxs-lookup"><span data-stu-id="d09c6-118">-AllVersions</span></span>
<span data-ttu-id="d09c6-119">Gibt an, dass dieses Cmdlet alle Versionen einer Erweiterung auflistet.</span><span class="sxs-lookup"><span data-stu-id="d09c6-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

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

### <span data-ttu-id="d09c6-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="d09c6-120">-ExtensionName</span></span>
<span data-ttu-id="d09c6-121">Gibt den Namen der verfügbaren Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d09c6-121">Specifies the name of the available extension.</span></span>

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

### <span data-ttu-id="d09c6-122">-Information</span><span class="sxs-lookup"><span data-stu-id="d09c6-122">-InformationAction</span></span>
<span data-ttu-id="d09c6-123">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="d09c6-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d09c6-124">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d09c6-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d09c6-125">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="d09c6-125">Continue</span></span>
- <span data-ttu-id="d09c6-126">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="d09c6-126">Ignore</span></span>
- <span data-ttu-id="d09c6-127">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="d09c6-127">Inquire</span></span>
- <span data-ttu-id="d09c6-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d09c6-128">SilentlyContinue</span></span>
- <span data-ttu-id="d09c6-129">Beenden</span><span class="sxs-lookup"><span data-stu-id="d09c6-129">Stop</span></span>
- <span data-ttu-id="d09c6-130">Anhalten</span><span class="sxs-lookup"><span data-stu-id="d09c6-130">Suspend</span></span>

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

### <span data-ttu-id="d09c6-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d09c6-131">-InformationVariable</span></span>
<span data-ttu-id="d09c6-132">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="d09c6-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d09c6-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="d09c6-133">-Profile</span></span>
<span data-ttu-id="d09c6-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="d09c6-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d09c6-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="d09c6-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d09c6-136">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d09c6-136">-Publisher</span></span>
<span data-ttu-id="d09c6-137">Gibt den Herausgeber der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d09c6-137">Specifies the publisher of the extension.</span></span>

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

### <span data-ttu-id="d09c6-138">-Version</span><span class="sxs-lookup"><span data-stu-id="d09c6-138">-Version</span></span>
<span data-ttu-id="d09c6-139">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="d09c6-139">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="d09c6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d09c6-140">CommonParameters</span></span>
<span data-ttu-id="d09c6-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d09c6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d09c6-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d09c6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d09c6-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d09c6-143">INPUTS</span></span>

## <span data-ttu-id="d09c6-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d09c6-144">OUTPUTS</span></span>

## <span data-ttu-id="d09c6-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="d09c6-145">NOTES</span></span>

## <span data-ttu-id="d09c6-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d09c6-146">RELATED LINKS</span></span>

