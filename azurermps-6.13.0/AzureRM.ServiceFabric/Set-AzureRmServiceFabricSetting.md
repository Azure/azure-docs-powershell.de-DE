---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 42d643faa1b3047c6ee2e3266a68a2ce692ec676
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497297"
---
# <span data-ttu-id="17231-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="17231-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="17231-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="17231-102">SYNOPSIS</span></span>
<span data-ttu-id="17231-103">Hinzufügen oder Aktualisieren einer oder mehrerer Service Fabric-Einstellungen zum Cluster</span><span class="sxs-lookup"><span data-stu-id="17231-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17231-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="17231-104">SYNTAX</span></span>

### <span data-ttu-id="17231-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="17231-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17231-106">Batch Einstellungen</span><span class="sxs-lookup"><span data-stu-id="17231-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17231-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17231-107">DESCRIPTION</span></span>
<span data-ttu-id="17231-108">Verwenden Sie "AzureRmServiceFabricSetting", um Dienst Fabric **-** Einstellungen in einem Cluster hinzuzufügen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="17231-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="17231-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17231-109">EXAMPLES</span></span>

### <span data-ttu-id="17231-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17231-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="17231-111">Mit diesem Befehl wird "MaxFileOperationTimeout" auf den Wert "5000" im Abschnitt "NamingService" gesetzt.</span><span class="sxs-lookup"><span data-stu-id="17231-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="17231-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="17231-112">PARAMETERS</span></span>

### <span data-ttu-id="17231-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17231-113">-DefaultProfile</span></span>
<span data-ttu-id="17231-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="17231-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17231-115">-Name</span><span class="sxs-lookup"><span data-stu-id="17231-115">-Name</span></span>
<span data-ttu-id="17231-116">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="17231-116">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17231-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="17231-117">-Parameter</span></span>
<span data-ttu-id="17231-118">Parameter.</span><span class="sxs-lookup"><span data-stu-id="17231-118">Parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17231-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17231-119">-ResourceGroupName</span></span>
<span data-ttu-id="17231-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="17231-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17231-121">-Section</span><span class="sxs-lookup"><span data-stu-id="17231-121">-Section</span></span>
<span data-ttu-id="17231-122">Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="17231-122">Section.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17231-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="17231-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="17231-124">Client Authentifizierungs.</span><span class="sxs-lookup"><span data-stu-id="17231-124">Client authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17231-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="17231-125">-Value</span></span>
<span data-ttu-id="17231-126">Wert.</span><span class="sxs-lookup"><span data-stu-id="17231-126">Value.</span></span>

```yaml
Type: System.String
Parameter Sets: OneSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17231-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17231-127">-Confirm</span></span>
<span data-ttu-id="17231-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17231-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17231-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17231-129">-WhatIf</span></span>
<span data-ttu-id="17231-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17231-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17231-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17231-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17231-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17231-132">CommonParameters</span></span>
<span data-ttu-id="17231-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17231-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17231-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17231-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17231-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="17231-135">INPUTS</span></span>

### <span data-ttu-id="17231-136">System. String</span><span class="sxs-lookup"><span data-stu-id="17231-136">System.String</span></span>
<span data-ttu-id="17231-137">Parameter: Parameter (ByValue), Abschnitt (ByValue), Wert (ByValue)</span><span class="sxs-lookup"><span data-stu-id="17231-137">Parameters: Parameter (ByValue), Section (ByValue), Value (ByValue)</span></span>

### <span data-ttu-id="17231-138">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="17231-138">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>
<span data-ttu-id="17231-139">Parameter: SettingsSectionDescription (ByValue)</span><span class="sxs-lookup"><span data-stu-id="17231-139">Parameters: SettingsSectionDescription (ByValue)</span></span>

## <span data-ttu-id="17231-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="17231-140">OUTPUTS</span></span>

### <span data-ttu-id="17231-141">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="17231-141">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="17231-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="17231-142">NOTES</span></span>

## <span data-ttu-id="17231-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="17231-143">RELATED LINKS</span></span>
