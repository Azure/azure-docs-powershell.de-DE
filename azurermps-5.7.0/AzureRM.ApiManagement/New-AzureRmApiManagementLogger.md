---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2929cbd89328d971b47b748d4aa042ade13c1af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483181"
---
# <span data-ttu-id="c4ee7-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ee7-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="c4ee7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4ee7-102">SYNOPSIS</span></span>
<span data-ttu-id="c4ee7-103">Erstellt eine API-verwaltungsprotokollierung.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4ee7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4ee7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4ee7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4ee7-105">DESCRIPTION</span></span>
<span data-ttu-id="c4ee7-106">Das Cmdlet **New-AzureRmApiManagementLogger** erstellt eine Azure API-Verwaltungs **Protokollierung**.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="c4ee7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4ee7-107">EXAMPLES</span></span>

### <span data-ttu-id="c4ee7-108">Beispiel 1: Erstellen einer Protokollierung</span><span class="sxs-lookup"><span data-stu-id="c4ee7-108">Example 1: Create a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="c4ee7-109">Dieser Befehl erstellt eine Protokollierung mit dem Namen ContosoSdkEventHub mithilfe der angegebenen Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="c4ee7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4ee7-110">PARAMETERS</span></span>

### <span data-ttu-id="c4ee7-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="c4ee7-111">-ConnectionString</span></span>
<span data-ttu-id="c4ee7-112">Gibt eine Azure Event Hubs-Verbindungszeichenfolge an, die mit den folgenden Schritten beginnt:</span><span class="sxs-lookup"><span data-stu-id="c4ee7-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="c4ee7-113">Der Schlüssel mit den Sende rechten in der Verbindungszeichenfolge muss konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-113">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee7-114">-Context</span><span class="sxs-lookup"><span data-stu-id="c4ee7-114">-Context</span></span>
<span data-ttu-id="c4ee7-115">Gibt ein **PsApiManagementContext** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4ee7-116">-DefaultProfile</span></span>
<span data-ttu-id="c4ee7-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c4ee7-118">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4ee7-118">-Description</span></span>
<span data-ttu-id="c4ee7-119">Gibt eine Beschreibung an.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-119">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee7-120">-Isgepuffert</span><span class="sxs-lookup"><span data-stu-id="c4ee7-120">-IsBuffered</span></span>
<span data-ttu-id="c4ee7-121">Gibt an, ob die Datensätze in der Protokollierung vor der Veröffentlichung gepuffert werden.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-121">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="c4ee7-122">Der Standardwert ist $true.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-122">The default value is $True.</span></span>
<span data-ttu-id="c4ee7-123">Wenn Datensätze gepuffert werden, werden Sie alle 15 Sekunden an Ereignis Hubs gesendet, oder wenn der Puffer 256 KB Nachrichten empfängt.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-123">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee7-124">-Protokollierungs-Nr</span><span class="sxs-lookup"><span data-stu-id="c4ee7-124">-LoggerId</span></span>
<span data-ttu-id="c4ee7-125">Gibt eine ID für die Protokollierung an.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-125">Specifies an ID for the logger.</span></span>
<span data-ttu-id="c4ee7-126">Wenn Sie keine ID angeben, generiert dieses Cmdlet eine.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-126">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee7-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c4ee7-127">-Name</span></span>
<span data-ttu-id="c4ee7-128">Gibt den Entitätsnamen eines Ereignis Hubs aus dem Azure Classic-Portal an.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-128">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4ee7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4ee7-129">CommonParameters</span></span>
<span data-ttu-id="c4ee7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4ee7-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4ee7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4ee7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4ee7-132">INPUTS</span></span>

### <span data-ttu-id="c4ee7-133">Keine</span><span class="sxs-lookup"><span data-stu-id="c4ee7-133">None</span></span>
<span data-ttu-id="c4ee7-134">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c4ee7-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4ee7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4ee7-135">OUTPUTS</span></span>

### <span data-ttu-id="c4ee7-136">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ee7-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="c4ee7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4ee7-137">NOTES</span></span>

## <span data-ttu-id="c4ee7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4ee7-138">RELATED LINKS</span></span>

[<span data-ttu-id="c4ee7-139">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ee7-139">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c4ee7-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ee7-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="c4ee7-141">Satz-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="c4ee7-141">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


