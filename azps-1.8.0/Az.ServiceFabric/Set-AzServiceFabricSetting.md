---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricSetting.md
ms.openlocfilehash: cea8ec21021725bae99ef597a33079621f539cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659309"
---
# <span data-ttu-id="b751e-101">Set-AzServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="b751e-101">Set-AzServiceFabricSetting</span></span>

## <span data-ttu-id="b751e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b751e-102">SYNOPSIS</span></span>
<span data-ttu-id="b751e-103">Hinzufügen oder Aktualisieren einer oder mehrerer Service Fabric-Einstellungen zum Cluster</span><span class="sxs-lookup"><span data-stu-id="b751e-103">Add or update one or multiple Service Fabric settings to the cluster.</span></span>

## <span data-ttu-id="b751e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b751e-104">SYNTAX</span></span>

### <span data-ttu-id="b751e-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="b751e-105">OneSetting</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String> -Parameter <String>
 -Value <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b751e-106">Batch Einstellungen</span><span class="sxs-lookup"><span data-stu-id="b751e-106">BatchSettings</span></span>
```
Set-AzServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b751e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b751e-107">DESCRIPTION</span></span>
<span data-ttu-id="b751e-108">Verwenden Sie "AzServiceFabricSetting", um Dienst Fabric **-** Einstellungen in einem Cluster hinzuzufügen oder zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b751e-108">Use **Set-AzServiceFabricSetting** to add or update Service Fabric settings in a cluster.</span></span>

## <span data-ttu-id="b751e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b751e-109">EXAMPLES</span></span>

### <span data-ttu-id="b751e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b751e-110">Example 1</span></span>
```
PS c:\> Set-AzServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -Section 'NamingService' -Parameter 'MaxFileOperationTimeout' -Value 5000
```

<span data-ttu-id="b751e-111">Mit diesem Befehl wird "MaxFileOperationTimeout" auf den Wert "5000" im Abschnitt "NamingService" gesetzt.</span><span class="sxs-lookup"><span data-stu-id="b751e-111">This command will set 'MaxFileOperationTimeout' to value '5000' under the section 'NamingService'.</span></span>

## <span data-ttu-id="b751e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b751e-112">PARAMETERS</span></span>

### <span data-ttu-id="b751e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b751e-113">-DefaultProfile</span></span>
<span data-ttu-id="b751e-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b751e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b751e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b751e-115">-Name</span></span>
<span data-ttu-id="b751e-116">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="b751e-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b751e-117">-Parameter</span><span class="sxs-lookup"><span data-stu-id="b751e-117">-Parameter</span></span>
<span data-ttu-id="b751e-118">Parameter.</span><span class="sxs-lookup"><span data-stu-id="b751e-118">Parameter.</span></span>

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

### <span data-ttu-id="b751e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b751e-119">-ResourceGroupName</span></span>
<span data-ttu-id="b751e-120">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="b751e-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b751e-121">-Section</span><span class="sxs-lookup"><span data-stu-id="b751e-121">-Section</span></span>
<span data-ttu-id="b751e-122">Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="b751e-122">Section.</span></span>

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

### <span data-ttu-id="b751e-123">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="b751e-123">-SettingsSectionDescription</span></span>
<span data-ttu-id="b751e-124">Client Authentifizierungs.</span><span class="sxs-lookup"><span data-stu-id="b751e-124">Client authentication type.</span></span>

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

### <span data-ttu-id="b751e-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="b751e-125">-Value</span></span>
<span data-ttu-id="b751e-126">Wert.</span><span class="sxs-lookup"><span data-stu-id="b751e-126">Value.</span></span>

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

### <span data-ttu-id="b751e-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b751e-127">-Confirm</span></span>
<span data-ttu-id="b751e-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b751e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b751e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b751e-129">-WhatIf</span></span>
<span data-ttu-id="b751e-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b751e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b751e-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b751e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b751e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b751e-132">CommonParameters</span></span>
<span data-ttu-id="b751e-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b751e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b751e-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b751e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b751e-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b751e-135">INPUTS</span></span>

### <span data-ttu-id="b751e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b751e-136">System.String</span></span>

### <span data-ttu-id="b751e-137">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="b751e-137">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="b751e-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b751e-138">OUTPUTS</span></span>

### <span data-ttu-id="b751e-139">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="b751e-139">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b751e-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="b751e-140">NOTES</span></span>

## <span data-ttu-id="b751e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b751e-141">RELATED LINKS</span></span>
