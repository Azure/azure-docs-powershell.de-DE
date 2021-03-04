---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 030c97a05d7f87ffc75c284250e8b67e8d3dc1fb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101919915"
---
# <span data-ttu-id="4bd70-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="4bd70-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="4bd70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bd70-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd70-103">Erstellt einen neuen Exportgeräteauftrag.</span><span class="sxs-lookup"><span data-stu-id="4bd70-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="4bd70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4bd70-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4bd70-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bd70-105">DESCRIPTION</span></span>
<span data-ttu-id="4bd70-106">Erstellt einen neuen Exportgeräteauftrag für den IotHub.</span><span class="sxs-lookup"><span data-stu-id="4bd70-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="4bd70-107">Dadurch werden alle Geräte in den angegebenen Container exportiert.</span><span class="sxs-lookup"><span data-stu-id="4bd70-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="4bd70-108">Lesen Sie den folgenden Artikel zum Generieren des SAS-URI.</span><span class="sxs-lookup"><span data-stu-id="4bd70-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="4bd70-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="4bd70-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="4bd70-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4bd70-110">EXAMPLES</span></span>

### <span data-ttu-id="4bd70-111">Beispiel 1: Problem einer Exportgeräteanforderung.</span><span class="sxs-lookup"><span data-stu-id="4bd70-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="4bd70-112">Erstellt eine neue Exportgeräteanforderung für den IotHub "myiothub" mit Ausnahme der Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="4bd70-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="4bd70-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4bd70-113">PARAMETERS</span></span>

### <span data-ttu-id="4bd70-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd70-114">-DefaultProfile</span></span>
<span data-ttu-id="4bd70-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4bd70-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4bd70-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="4bd70-116">-ExcludeKeys</span></span>
<span data-ttu-id="4bd70-117">Ermöglicht das Exportieren von Geräten ohne Tasten.</span><span class="sxs-lookup"><span data-stu-id="4bd70-117">Allows to export devices without keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd70-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="4bd70-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="4bd70-119">Der URI, in den das Blob exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bd70-119">The Uri to export the blob to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd70-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4bd70-120">-Name</span></span>
<span data-ttu-id="4bd70-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="4bd70-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bd70-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd70-122">-ResourceGroupName</span></span>
<span data-ttu-id="4bd70-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="4bd70-123">Resource Group Name</span></span>

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

### <span data-ttu-id="4bd70-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4bd70-124">-Confirm</span></span>
<span data-ttu-id="4bd70-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4bd70-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd70-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bd70-126">-WhatIf</span></span>
<span data-ttu-id="4bd70-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4bd70-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4bd70-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4bd70-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bd70-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd70-129">CommonParameters</span></span>
<span data-ttu-id="4bd70-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd70-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd70-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd70-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd70-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4bd70-132">INPUTS</span></span>

### <span data-ttu-id="4bd70-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4bd70-133">System.String</span></span>

## <span data-ttu-id="4bd70-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4bd70-134">OUTPUTS</span></span>

### <span data-ttu-id="4bd70-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="4bd70-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="4bd70-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4bd70-136">NOTES</span></span>

## <span data-ttu-id="4bd70-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4bd70-137">RELATED LINKS</span></span>
