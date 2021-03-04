---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: f2a2daebcb77746ae087fe527245376963fade5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101920691"
---
# <span data-ttu-id="86148-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="86148-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="86148-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86148-102">SYNOPSIS</span></span>
<span data-ttu-id="86148-103">Erstellt einen neuen Importgeräteauftrag.</span><span class="sxs-lookup"><span data-stu-id="86148-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="86148-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86148-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86148-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86148-105">DESCRIPTION</span></span>
<span data-ttu-id="86148-106">Erstellt einen neuen Importgeräteauftrag für den IotHub.</span><span class="sxs-lookup"><span data-stu-id="86148-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="86148-107">Dadurch werden alle Geräte aus dem angegebenen Container in den IotHub importiert.</span><span class="sxs-lookup"><span data-stu-id="86148-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="86148-108">Lesen Sie den folgenden Artikel zum Generieren des SAS-URI.</span><span class="sxs-lookup"><span data-stu-id="86148-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="86148-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="86148-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="86148-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="86148-110">EXAMPLES</span></span>

### <span data-ttu-id="86148-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="86148-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="86148-112">Erstellt eine neue Importgeräteanforderung für den IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="86148-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="86148-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="86148-113">PARAMETERS</span></span>

### <span data-ttu-id="86148-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86148-114">-DefaultProfile</span></span>
<span data-ttu-id="86148-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="86148-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86148-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="86148-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="86148-117">Input Blob Container Uri für FileUpload</span><span class="sxs-lookup"><span data-stu-id="86148-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="86148-118">-Name</span><span class="sxs-lookup"><span data-stu-id="86148-118">-Name</span></span>
<span data-ttu-id="86148-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="86148-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="86148-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="86148-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="86148-121">Der URI, in den die Ausgabe geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="86148-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="86148-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86148-122">-ResourceGroupName</span></span>
<span data-ttu-id="86148-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="86148-123">Resource Group Name</span></span>

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

### <span data-ttu-id="86148-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86148-124">-Confirm</span></span>
<span data-ttu-id="86148-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86148-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86148-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86148-126">-WhatIf</span></span>
<span data-ttu-id="86148-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86148-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86148-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86148-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86148-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86148-129">CommonParameters</span></span>
<span data-ttu-id="86148-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86148-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86148-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86148-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86148-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="86148-132">INPUTS</span></span>

### <span data-ttu-id="86148-133">System.String</span><span class="sxs-lookup"><span data-stu-id="86148-133">System.String</span></span>

## <span data-ttu-id="86148-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="86148-134">OUTPUTS</span></span>

### <span data-ttu-id="86148-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="86148-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="86148-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="86148-136">NOTES</span></span>

## <span data-ttu-id="86148-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="86148-137">RELATED LINKS</span></span>
