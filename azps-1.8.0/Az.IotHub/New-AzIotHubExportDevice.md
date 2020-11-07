---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 72c0793f75e00ec46a27cda476163f7cc0c93090
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819743"
---
# <span data-ttu-id="a460d-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="a460d-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="a460d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a460d-102">SYNOPSIS</span></span>
<span data-ttu-id="a460d-103">Erstellt einen neuen Auftrag für Export Geräte.</span><span class="sxs-lookup"><span data-stu-id="a460d-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="a460d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a460d-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a460d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a460d-105">DESCRIPTION</span></span>
<span data-ttu-id="a460d-106">Erstellt einen neuen Export Geräte Auftrag für die IotHub.</span><span class="sxs-lookup"><span data-stu-id="a460d-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="a460d-107">Dadurch werden alle Geräte in den angegebenen Container exportiert.</span><span class="sxs-lookup"><span data-stu-id="a460d-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="a460d-108">Lesen Sie den folgenden Artikel zum Generieren des SAS-URIs.</span><span class="sxs-lookup"><span data-stu-id="a460d-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="a460d-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="a460d-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="a460d-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a460d-110">EXAMPLES</span></span>

### <span data-ttu-id="a460d-111">Beispiel 1: eine Export Geräteanforderung ausgeben.</span><span class="sxs-lookup"><span data-stu-id="a460d-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="a460d-112">Erstellt eine neue Export Geräteanforderung für das IotHub "myiothub", wobei die Schlüssel ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a460d-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="a460d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a460d-113">PARAMETERS</span></span>

### <span data-ttu-id="a460d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a460d-114">-DefaultProfile</span></span>
<span data-ttu-id="a460d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a460d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a460d-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="a460d-116">-ExcludeKeys</span></span>
<span data-ttu-id="a460d-117">Ermöglicht das Exportieren von Geräten ohne Tasten.</span><span class="sxs-lookup"><span data-stu-id="a460d-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="a460d-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a460d-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="a460d-119">Der URI, in den das BLOB exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a460d-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="a460d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a460d-120">-Name</span></span>
<span data-ttu-id="a460d-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="a460d-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="a460d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a460d-122">-ResourceGroupName</span></span>
<span data-ttu-id="a460d-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a460d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a460d-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a460d-124">-Confirm</span></span>
<span data-ttu-id="a460d-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a460d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a460d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a460d-126">-WhatIf</span></span>
<span data-ttu-id="a460d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a460d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a460d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a460d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a460d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a460d-129">CommonParameters</span></span>
<span data-ttu-id="a460d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a460d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a460d-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a460d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a460d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a460d-132">INPUTS</span></span>

### <span data-ttu-id="a460d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a460d-133">System.String</span></span>

## <span data-ttu-id="a460d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a460d-134">OUTPUTS</span></span>

### <span data-ttu-id="a460d-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="a460d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="a460d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a460d-136">NOTES</span></span>

## <span data-ttu-id="a460d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a460d-137">RELATED LINKS</span></span>
