---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: c21c227dd748f28523f4ac616d003e029d19e38f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499277"
---
# <span data-ttu-id="dd535-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dd535-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="dd535-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd535-102">SYNOPSIS</span></span>
<span data-ttu-id="dd535-103">Ändert eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="dd535-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd535-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd535-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd535-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd535-105">DESCRIPTION</span></span>
<span data-ttu-id="dd535-106">Das Cmdlet " **festlegen-AzureRmApiManagementLogger** " ändert die Einstellungen einer Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="dd535-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="dd535-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd535-107">EXAMPLES</span></span>

### <span data-ttu-id="dd535-108">Beispiel 1: Ändern einer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="dd535-108">Example 1: Modify a logger</span></span>
```
PS C:\>Set-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="dd535-109">Mit diesem Befehl wird eine Protokollierung geändert, die die ID Logger123.</span><span class="sxs-lookup"><span data-stu-id="dd535-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="dd535-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd535-110">PARAMETERS</span></span>

### <span data-ttu-id="dd535-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="dd535-111">-ConnectionString</span></span>
<span data-ttu-id="dd535-112">Gibt eine Azure Event Hubs-Verbindungszeichenfolge an, die Sende Richtlinienrechte umfasst.</span><span class="sxs-lookup"><span data-stu-id="dd535-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd535-113">-Context</span><span class="sxs-lookup"><span data-stu-id="dd535-113">-Context</span></span>
<span data-ttu-id="dd535-114">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="dd535-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd535-115">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd535-115">-Description</span></span>
<span data-ttu-id="dd535-116">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="dd535-116">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd535-117">-Isgepuffert</span><span class="sxs-lookup"><span data-stu-id="dd535-117">-IsBuffered</span></span>
<span data-ttu-id="dd535-118">Gibt an, dass die Datensätze in der Protokollierung vor der Veröffentlichung gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="dd535-118">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="dd535-119">Wenn Datensätze gepuffert werden, werden Sie alle 15 Sekunden an Ereignis Hubs gesendet, oder wenn der Puffer 256 KB Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="dd535-119">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd535-120">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="dd535-120">-LoggerId</span></span>
<span data-ttu-id="dd535-121">Gibt die ID der Protokollierung an, die aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="dd535-121">Specifies the ID of the logger to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd535-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dd535-122">-Name</span></span>
<span data-ttu-id="dd535-123">Gibt den Entitätsnamen eines Ereignis Hubs aus dem Azure Classic-Portal an.</span><span class="sxs-lookup"><span data-stu-id="dd535-123">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd535-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd535-124">-PassThru</span></span>
<span data-ttu-id="dd535-125">Gibt an, dass dieses Cmdlet die  **PsApiManagementLogger** zurückgibt, die von diesem Cmdlet geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dd535-125">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd535-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd535-126">-DefaultProfile</span></span>
<span data-ttu-id="dd535-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd535-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd535-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd535-128">CommonParameters</span></span>
<span data-ttu-id="dd535-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd535-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd535-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd535-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd535-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd535-131">INPUTS</span></span>

## <span data-ttu-id="dd535-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd535-132">OUTPUTS</span></span>

### <span data-ttu-id="dd535-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dd535-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="dd535-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd535-134">NOTES</span></span>

## <span data-ttu-id="dd535-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd535-135">RELATED LINKS</span></span>

[<span data-ttu-id="dd535-136">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dd535-136">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="dd535-137">Neu – AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dd535-137">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="dd535-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="dd535-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


