---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricSetting.md
ms.openlocfilehash: 6fe4d0c3a32cd96693d64e46f9d8596083dd9c5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481546"
---
# <span data-ttu-id="75689-101">Remove-AzureRmServiceFabricSetting</span><span class="sxs-lookup"><span data-stu-id="75689-101">Remove-AzureRmServiceFabricSetting</span></span>

## <span data-ttu-id="75689-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75689-102">SYNOPSIS</span></span>
<span data-ttu-id="75689-103">Entfernen einer oder mehrerer Service Fabric-Einstellungen aus dem Cluster</span><span class="sxs-lookup"><span data-stu-id="75689-103">Remove one or multiple Service Fabric setting from the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75689-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75689-104">SYNTAX</span></span>

### <span data-ttu-id="75689-105">OneSetting</span><span class="sxs-lookup"><span data-stu-id="75689-105">OneSetting</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String> -Section <String>
 -Parameter <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75689-106">Batch Einstellungen</span><span class="sxs-lookup"><span data-stu-id="75689-106">BatchSettings</span></span>
```
Remove-AzureRmServiceFabricSetting [-ResourceGroupName] <String> [-Name] <String>
 -SettingsSectionDescription <PSSettingsSectionDescription[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75689-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75689-107">DESCRIPTION</span></span>
<span data-ttu-id="75689-108">Verwenden **Sie Remove-AzureRmServiceFabricSetting** , um die Service Fabric-Einstellungen aus dem Cluster zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="75689-108">Use **Remove-AzureRmServiceFabricSetting** to remove Service Fabric settings from the cluster.</span></span>

## <span data-ttu-id="75689-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75689-109">EXAMPLES</span></span>

### <span data-ttu-id="75689-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75689-110">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricSetting -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Section 'EseStore' -Parameter 'MaxCursors'
```

<span data-ttu-id="75689-111">Dieser Befehl entfernt die Einstellungen "MaxCursors" unter "EseStore".</span><span class="sxs-lookup"><span data-stu-id="75689-111">This command will remove settings 'MaxCursors' under 'EseStore' section.</span></span>

## <span data-ttu-id="75689-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="75689-112">PARAMETERS</span></span>

### <span data-ttu-id="75689-113">-Name</span><span class="sxs-lookup"><span data-stu-id="75689-113">-Name</span></span>
<span data-ttu-id="75689-114">Geben Sie den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="75689-114">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="75689-115">-Parameter</span><span class="sxs-lookup"><span data-stu-id="75689-115">-Parameter</span></span>
<span data-ttu-id="75689-116">Parameter.</span><span class="sxs-lookup"><span data-stu-id="75689-116">Parameter.</span></span>

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

### <span data-ttu-id="75689-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75689-117">-ResourceGroupName</span></span>
<span data-ttu-id="75689-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="75689-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="75689-119">-Section</span><span class="sxs-lookup"><span data-stu-id="75689-119">-Section</span></span>
<span data-ttu-id="75689-120">Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="75689-120">Section.</span></span>

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

### <span data-ttu-id="75689-121">-SettingsSectionDescription</span><span class="sxs-lookup"><span data-stu-id="75689-121">-SettingsSectionDescription</span></span>
<span data-ttu-id="75689-122">Client Authentifizierungs.</span><span class="sxs-lookup"><span data-stu-id="75689-122">Client authentication type.</span></span>

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

### <span data-ttu-id="75689-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75689-123">-Confirm</span></span>
<span data-ttu-id="75689-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75689-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75689-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75689-125">-WhatIf</span></span>
<span data-ttu-id="75689-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75689-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75689-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75689-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75689-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75689-128">-DefaultProfile</span></span>
<span data-ttu-id="75689-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75689-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75689-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75689-130">CommonParameters</span></span>
<span data-ttu-id="75689-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75689-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75689-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75689-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75689-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75689-133">INPUTS</span></span>

### <span data-ttu-id="75689-134">System. String</span><span class="sxs-lookup"><span data-stu-id="75689-134">System.String</span></span>
<span data-ttu-id="75689-135">Microsoft. Azure. Commands. ServiceFabric. Models. PSSettingsSectionDescription []</span><span class="sxs-lookup"><span data-stu-id="75689-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSSettingsSectionDescription[]</span></span>

## <span data-ttu-id="75689-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75689-136">OUTPUTS</span></span>

### <span data-ttu-id="75689-137">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="75689-137">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="75689-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="75689-138">NOTES</span></span>

## <span data-ttu-id="75689-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75689-139">RELATED LINKS</span></span>

