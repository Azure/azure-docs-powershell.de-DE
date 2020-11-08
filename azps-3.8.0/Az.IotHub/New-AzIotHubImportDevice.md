---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: bb1b5579869c7142bcf6cbe168ff10aaa9b7e083
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004013"
---
# <span data-ttu-id="a5b58-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="a5b58-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="a5b58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5b58-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b58-103">Erstellt einen neuen Auftrag für Import Geräte.</span><span class="sxs-lookup"><span data-stu-id="a5b58-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="a5b58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5b58-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b58-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5b58-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b58-106">Erstellt einen neuen Import Geräte Auftrag für die IotHub.</span><span class="sxs-lookup"><span data-stu-id="a5b58-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="a5b58-107">Dadurch werden alle Geräte aus dem angegebenen Container in den IotHub-Container importiert.</span><span class="sxs-lookup"><span data-stu-id="a5b58-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="a5b58-108">Lesen Sie den folgenden Artikel zum Generieren des SAS-URIs.</span><span class="sxs-lookup"><span data-stu-id="a5b58-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="a5b58-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="a5b58-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="a5b58-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5b58-110">EXAMPLES</span></span>

### <span data-ttu-id="a5b58-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5b58-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="a5b58-112">Erstellt eine neue Import Geräteanforderung für das IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="a5b58-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="a5b58-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5b58-113">PARAMETERS</span></span>

### <span data-ttu-id="a5b58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b58-114">-DefaultProfile</span></span>
<span data-ttu-id="a5b58-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a5b58-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5b58-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a5b58-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="a5b58-117">Eingabe-BLOB-Container-URI für FileUpload</span><span class="sxs-lookup"><span data-stu-id="a5b58-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="a5b58-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a5b58-118">-Name</span></span>
<span data-ttu-id="a5b58-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="a5b58-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="a5b58-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="a5b58-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="a5b58-121">Der URI, in den die Ausgabe geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5b58-121">The Uri to write the output to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b58-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b58-122">-ResourceGroupName</span></span>
<span data-ttu-id="a5b58-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a5b58-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a5b58-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5b58-124">-Confirm</span></span>
<span data-ttu-id="a5b58-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5b58-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b58-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b58-126">-WhatIf</span></span>
<span data-ttu-id="a5b58-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5b58-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b58-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5b58-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b58-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b58-129">CommonParameters</span></span>
<span data-ttu-id="a5b58-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b58-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b58-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b58-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b58-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5b58-132">INPUTS</span></span>

### <span data-ttu-id="a5b58-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a5b58-133">System.String</span></span>

## <span data-ttu-id="a5b58-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5b58-134">OUTPUTS</span></span>

### <span data-ttu-id="a5b58-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="a5b58-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="a5b58-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5b58-136">NOTES</span></span>

## <span data-ttu-id="a5b58-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5b58-137">RELATED LINKS</span></span>
