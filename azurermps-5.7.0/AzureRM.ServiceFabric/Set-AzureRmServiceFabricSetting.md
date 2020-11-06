---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/set-azurermservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Set-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 8296945de2bcf98213fc692e486e793a91f84939
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478221"
---
# <span data-ttu-id="0dd52-101">Set-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="0dd52-101">Set-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="0dd52-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0dd52-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd52-103">Hinzufügen oder Aktualisieren einer oder mehrerer Service Fabric-Einstellungen zum Cluster</span><span class="sxs-lookup"><span data-stu-id="0dd52-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0dd52-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dd52-104">SYNTAX</span></span>

### <span data-ttu-id="0dd52-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="0dd52-105">OneSetting</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0dd52-106">Batch Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0dd52-106">BatchSettings</span></span>
```
Set-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dd52-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0dd52-107">DESCRIPTION</span></span>
<span data-ttu-id="0dd52-108">Verwenden Sie "AzureRmServiceFabricSetting", um Dienst Fabric **-** Einstellungen in einem Cluster hinzuzufügen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="0dd52-108">Use **Set-AzureRmServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="0dd52-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0dd52-109">EXAMPLES</span></span>

### <span data-ttu-id="0dd52-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0dd52-110">Example 1</span></span>
```
PS c:\> Set-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="0dd52-111">Mit diesem Befehl wird "MaxFileOperationTimeout" auf den Wert "5000" im Abschnitt "NamingService" gesetzt.</span><span class="sxs-lookup"><span data-stu-id="0dd52-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="0dd52-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dd52-112">PARAMETERS</span></span>

### <span data-ttu-id="0dd52-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd52-113">-DefaultProfile</span></span>
<span data-ttu-id="0dd52-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0dd52-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd52-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0dd52-115">-Name</span></span>
<span data-ttu-id="0dd52-116">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="0dd52-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd52-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="0dd52-117">-Parameter</span></span>
<span data-ttu-id="0dd52-118">Parameter.</span><span class="sxs-lookup"><span data-stu-id="0dd52-118">Parameter.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd52-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dd52-119">-ResourceGroupName</span></span>
<span data-ttu-id="0dd52-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0dd52-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd52-121">-Section</span><span class="sxs-lookup"><span data-stu-id="0dd52-121">-Section</span></span>
<span data-ttu-id="0dd52-122">Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="0dd52-122">Section.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd52-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="0dd52-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="0dd52-124">Client Authentifizierungs.</span><span class="sxs-lookup"><span data-stu-id="0dd52-124">Client authentication type.</span></span>

```yaml
Type: PSSettingsSectionDescription[]
Parameter Sets: BatchSettings
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd52-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="0dd52-125">-Value</span></span>
<span data-ttu-id="0dd52-126">Wert.</span><span class="sxs-lookup"><span data-stu-id="0dd52-126">Value.</span></span>

```yaml
Type: String
Parameter Sets: OneSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0dd52-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0dd52-127">-Confirm</span></span>
<span data-ttu-id="0dd52-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0dd52-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd52-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dd52-129">-WhatIf</span></span>
<span data-ttu-id="0dd52-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dd52-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0dd52-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dd52-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd52-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd52-132">CommonParameters</span></span>
<span data-ttu-id="0dd52-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dd52-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd52-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dd52-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd52-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0dd52-135">INPUTS</span></span>

### <span data-ttu-id="0dd52-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0dd52-136">System.String</span></span>
<span data-ttu-id="0dd52-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="0dd52-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="0dd52-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0dd52-138">OUTPUTS</span></span>

### <span data-ttu-id="0dd52-139">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="0dd52-139">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="0dd52-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="0dd52-140">NOTES</span></span>

## <span data-ttu-id="0dd52-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0dd52-141">RELATED LINKS</span></span>

