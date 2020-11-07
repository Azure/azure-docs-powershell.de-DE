---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658229"
---
# <span data-ttu-id="a8311-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="a8311-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="a8311-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8311-102">SYNOPSIS</span></span>
<span data-ttu-id="a8311-103">Erstellt eine Instanz von PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="a8311-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="a8311-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8311-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8311-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8311-105">DESCRIPTION</span></span>
<span data-ttu-id="a8311-106">Hilfsbefehl zum Erstellen einer Instanz von PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="a8311-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="a8311-107">Dieser Befehl ist mit New-AzApiManagement Befehl zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8311-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="a8311-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8311-108">EXAMPLES</span></span>

### <span data-ttu-id="a8311-109">Beispiel 1: Erstellen einer SSL-Einstellung zum Aktivieren von TLS 1,0 auf Back-End und Frontend</span><span class="sxs-lookup"><span data-stu-id="a8311-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="a8311-110">Erstellen Sie eine neue Instanz von PsApiManagementSslSetting, um TLSv 1,0 sowohl im Frontend (zwischen Client und APIM) als auch im Back-End (zwischen APIM und Back-End) des ApiManagement-Gateways zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a8311-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="a8311-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8311-111">PARAMETERS</span></span>

### <span data-ttu-id="a8311-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="a8311-112">-BackendProtocol</span></span>
<span data-ttu-id="a8311-113">Back-End-Sicherheitsprotokolleinstellungen.</span><span class="sxs-lookup"><span data-stu-id="a8311-113">Backend Security protocol settings.</span></span> <span data-ttu-id="a8311-114">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8311-114">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8311-115">-Verarbeitet Neuvereinbarungen</span><span class="sxs-lookup"><span data-stu-id="a8311-115">-CipherSuite</span></span>
<span data-ttu-id="a8311-116">Einstellungen für SSL-Verschlüsselungs Pakete in der angegebenen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="a8311-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="a8311-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8311-117">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8311-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8311-118">-DefaultProfile</span></span>
<span data-ttu-id="a8311-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8311-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8311-120">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="a8311-120">-FrontendProtocol</span></span>
<span data-ttu-id="a8311-121">Einstellungen für das Frontend-Sicherheitsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="a8311-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="a8311-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8311-122">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8311-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="a8311-123">-ServerProtocol</span></span>
<span data-ttu-id="a8311-124">Server Protokolleinstellungen wie Http2.</span><span class="sxs-lookup"><span data-stu-id="a8311-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="a8311-125">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="a8311-125">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8311-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8311-126">CommonParameters</span></span>
<span data-ttu-id="a8311-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8311-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8311-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8311-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8311-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8311-129">INPUTS</span></span>

### <span data-ttu-id="a8311-130">Keine</span><span class="sxs-lookup"><span data-stu-id="a8311-130">None</span></span>

## <span data-ttu-id="a8311-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8311-131">OUTPUTS</span></span>

### <span data-ttu-id="a8311-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="a8311-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="a8311-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8311-133">NOTES</span></span>

## <span data-ttu-id="a8311-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8311-134">RELATED LINKS</span></span>

[<span data-ttu-id="a8311-135">Neu – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a8311-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

