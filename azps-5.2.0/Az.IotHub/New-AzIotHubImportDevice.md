---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubimportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubImportDevice.md
ms.openlocfilehash: bb1b5579869c7142bcf6cbe168ff10aaa9b7e083
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291934"
---
# <span data-ttu-id="f586f-101">New-AzIotHubImportDevice</span><span class="sxs-lookup"><span data-stu-id="f586f-101">New-AzIotHubImportDevice</span></span>

## <span data-ttu-id="f586f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f586f-102">SYNOPSIS</span></span>
<span data-ttu-id="f586f-103">Erstellt einen neuen Importgeräteauftrag.</span><span class="sxs-lookup"><span data-stu-id="f586f-103">Creates a new import devices job.</span></span>

## <span data-ttu-id="f586f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f586f-104">SYNTAX</span></span>

```
New-AzIotHubImportDevice [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f586f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f586f-105">DESCRIPTION</span></span>
<span data-ttu-id="f586f-106">Erstellt einen neuen Importgeräteauftrag für IotHub.</span><span class="sxs-lookup"><span data-stu-id="f586f-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="f586f-107">Dadurch werden alle Geräte aus dem angegebenen Container in IotHub importiert.</span><span class="sxs-lookup"><span data-stu-id="f586f-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="f586f-108">Informationen zum Generieren des SAS-URI finden Sie im folgenden Artikel.</span><span class="sxs-lookup"><span data-stu-id="f586f-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="f586f-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="f586f-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="f586f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f586f-110">EXAMPLES</span></span>

### <span data-ttu-id="f586f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f586f-111">Example 1</span></span>
```
PS C:\> New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="f586f-112">Erstellt eine neue Importgeräteanforderung für IotHub "myiothub".</span><span class="sxs-lookup"><span data-stu-id="f586f-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="f586f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f586f-113">PARAMETERS</span></span>

### <span data-ttu-id="f586f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f586f-114">-DefaultProfile</span></span>
<span data-ttu-id="f586f-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f586f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f586f-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f586f-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="f586f-117">Eingabe-BLOB-Container-URI für FileUpload</span><span class="sxs-lookup"><span data-stu-id="f586f-117">Input Blob Container Uri for FileUpload</span></span>

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

### <span data-ttu-id="f586f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f586f-118">-Name</span></span>
<span data-ttu-id="f586f-119">Name des IotHub</span><span class="sxs-lookup"><span data-stu-id="f586f-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="f586f-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f586f-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="f586f-121">Der URI, in den die Ausgabe geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="f586f-121">The Uri to write the output to.</span></span> 

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

### <span data-ttu-id="f586f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f586f-122">-ResourceGroupName</span></span>
<span data-ttu-id="f586f-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f586f-123">Resource Group Name</span></span>

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

### <span data-ttu-id="f586f-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f586f-124">-Confirm</span></span>
<span data-ttu-id="f586f-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f586f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f586f-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f586f-126">-WhatIf</span></span>
<span data-ttu-id="f586f-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f586f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f586f-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f586f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f586f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f586f-129">CommonParameters</span></span>
<span data-ttu-id="f586f-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f586f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f586f-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f586f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f586f-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f586f-132">INPUTS</span></span>

### <span data-ttu-id="f586f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f586f-133">System.String</span></span>

## <span data-ttu-id="f586f-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f586f-134">OUTPUTS</span></span>

### <span data-ttu-id="f586f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span><span class="sxs-lookup"><span data-stu-id="f586f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="f586f-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f586f-136">NOTES</span></span>

## <span data-ttu-id="f586f-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f586f-137">RELATED LINKS</span></span>
