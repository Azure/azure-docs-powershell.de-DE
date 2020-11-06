---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubexportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubExportDevices.md
ms.openlocfilehash: 4c13a6366f0ccae803e8020f16bf2b566bd70934
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497438"
---
# <span data-ttu-id="a42a5-101">New-AzureRmIotHubExportDevices</span><span class="sxs-lookup"><span data-stu-id="a42a5-101">New-AzureRmIotHubExportDevices</span></span>

## <span data-ttu-id="a42a5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a42a5-102">SYNOPSIS</span></span>
<span data-ttu-id="a42a5-103">Erstellt einen neuen Auftrag für Export Geräte.</span><span class="sxs-lookup"><span data-stu-id="a42a5-103">Creates a new export devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a42a5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a42a5-104">SYNTAX</span></span>

```
New-AzureRmIotHubExportDevices [-ResourceGroupName] <String> [-Name] <String>
 [-ExportBlobContainerUri] <String> [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a42a5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a42a5-105">DESCRIPTION</span></span>
<span data-ttu-id="a42a5-106">Erstellt einen neuen Export Geräte Auftrag für die IotHub.</span><span class="sxs-lookup"><span data-stu-id="a42a5-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="a42a5-107">Dadurch werden alle Geräte in den angegebenen Container exportiert.</span><span class="sxs-lookup"><span data-stu-id="a42a5-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="a42a5-108">Lesen Sie den folgenden Artikel zum Generieren des SAS-URIs.</span><span class="sxs-lookup"><span data-stu-id="a42a5-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="a42a5-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="a42a5-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="a42a5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a42a5-110">EXAMPLES</span></span>

### <span data-ttu-id="a42a5-111">Beispiel 1: eine Export Geräteanforderung ausgeben.</span><span class="sxs-lookup"><span data-stu-id="a42a5-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzureRmIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="a42a5-112">Erstellt eine neue Export Geräteanforderung für das IotHub "myiothub", wobei die Schlüssel ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="a42a5-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="a42a5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a42a5-113">PARAMETERS</span></span>

### <span data-ttu-id="a42a5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a42a5-114">-DefaultProfile</span></span>
<span data-ttu-id="a42a5-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a42a5-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a42a5-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="a42a5-116">-ExcludeKeys</span></span>
<span data-ttu-id="a42a5-117">Ermöglicht das Exportieren von Geräten ohne Tasten.</span><span class="sxs-lookup"><span data-stu-id="a42a5-117">Allows to export devices without keys.</span></span>

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

### <span data-ttu-id="a42a5-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a42a5-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="a42a5-119">Der URI, in den das BLOB exportiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a42a5-119">The Uri to export the blob to.</span></span> 

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

### <span data-ttu-id="a42a5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a42a5-120">-Name</span></span>
<span data-ttu-id="a42a5-121">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="a42a5-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="a42a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a42a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="a42a5-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a42a5-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a42a5-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a42a5-124">-Confirm</span></span>
<span data-ttu-id="a42a5-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a42a5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a42a5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a42a5-126">-WhatIf</span></span>
<span data-ttu-id="a42a5-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a42a5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a42a5-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a42a5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a42a5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42a5-129">CommonParameters</span></span>
<span data-ttu-id="a42a5-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a42a5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42a5-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a42a5-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42a5-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a42a5-132">INPUTS</span></span>

### <span data-ttu-id="a42a5-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a42a5-133">System.String</span></span>

## <span data-ttu-id="a42a5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a42a5-134">OUTPUTS</span></span>

### <span data-ttu-id="a42a5-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="a42a5-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="a42a5-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a42a5-136">NOTES</span></span>

## <span data-ttu-id="a42a5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a42a5-137">RELATED LINKS</span></span>
