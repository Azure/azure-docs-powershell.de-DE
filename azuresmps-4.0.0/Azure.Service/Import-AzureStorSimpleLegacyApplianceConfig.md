---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006465"
---
# <span data-ttu-id="ec47f-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="ec47f-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="ec47f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec47f-102">SYNOPSIS</span></span>
<span data-ttu-id="ec47f-103">Importiert eine Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="ec47f-103">Imports a configuration file.</span></span>

## <span data-ttu-id="ec47f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec47f-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ec47f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec47f-105">DESCRIPTION</span></span>
<span data-ttu-id="ec47f-106">Mit dem Cmdlet " **Import-AzureStorSimpleLegacyApplianceConfig** " wird die Konfigurationsdatei aus der Legacy Appliance importiert.</span><span class="sxs-lookup"><span data-stu-id="ec47f-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="ec47f-107">Diese Datei enthält Informationen zu Volumen Containern, Sicherungsrichtlinien und Speicherkonto Anmeldeinformationen für den Azure StorSimple-Dienst.</span><span class="sxs-lookup"><span data-stu-id="ec47f-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="ec47f-108">Dieses Cmdlet gibt die Konfigurationsmetadaten der Legacy Appliance zurück.</span><span class="sxs-lookup"><span data-stu-id="ec47f-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="ec47f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec47f-109">EXAMPLES</span></span>

### <span data-ttu-id="ec47f-110">Beispiel 1: Importieren einer Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="ec47f-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="ec47f-111">Mit diesem Befehl wird die Konfigurationsdatei im angegebenen Pfad importiert.</span><span class="sxs-lookup"><span data-stu-id="ec47f-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="ec47f-112">Der Befehl enthält den Schlüssel zum Entschlüsseln der Datei.</span><span class="sxs-lookup"><span data-stu-id="ec47f-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="ec47f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec47f-113">PARAMETERS</span></span>

### <span data-ttu-id="ec47f-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="ec47f-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="ec47f-115">Gibt den Entschlüsselungsschlüssel für die Konfiguration der Legacy-Appliance an.</span><span class="sxs-lookup"><span data-stu-id="ec47f-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="ec47f-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="ec47f-116">-ConfigFilePath</span></span>
<span data-ttu-id="ec47f-117">Gibt den absoluten Pfad der abzurufenden Konfigurationsdatei an.</span><span class="sxs-lookup"><span data-stu-id="ec47f-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec47f-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="ec47f-118">-Profile</span></span>
<span data-ttu-id="ec47f-119">Gibt ein Azure-Profil an.</span><span class="sxs-lookup"><span data-stu-id="ec47f-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ec47f-120">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="ec47f-120">-TargetDeviceName</span></span>
<span data-ttu-id="ec47f-121">Gibt den Namen des Zielgeräts an, wie es im Portal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ec47f-121">Specifies the name of the target device as presented in the portal.</span></span>

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

### <span data-ttu-id="ec47f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec47f-122">CommonParameters</span></span>
<span data-ttu-id="ec47f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec47f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec47f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec47f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec47f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec47f-125">INPUTS</span></span>

### <span data-ttu-id="ec47f-126">Keine</span><span class="sxs-lookup"><span data-stu-id="ec47f-126">None</span></span>

## <span data-ttu-id="ec47f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec47f-127">OUTPUTS</span></span>

### <span data-ttu-id="ec47f-128">LegacyApplianceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ec47f-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="ec47f-129">Dieses Cmdlet gibt die Details der Konfiguration zurück.</span><span class="sxs-lookup"><span data-stu-id="ec47f-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="ec47f-130">Das **LegacyApplianceConfiguration** -Objekt enthält die folgenden Informationen: Konfigurations-ID, Volumen Containernamen, Zugriffssteuerungseinträge, Sicherungsrichtlinien, Bandbreiteneinstellungen, Volumen Container, Anmeldeinformationen für das Speicherkonto und Volumes.</span><span class="sxs-lookup"><span data-stu-id="ec47f-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="ec47f-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec47f-131">NOTES</span></span>

## <span data-ttu-id="ec47f-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec47f-132">RELATED LINKS</span></span>

[<span data-ttu-id="ec47f-133">Importieren-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ec47f-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


