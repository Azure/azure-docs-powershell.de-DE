---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragecontext
schema: 2.0.0
ms.openlocfilehash: 3a91c88fe80151ef8aa3934c484cfe9b6671a750
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849827"
---
# <span data-ttu-id="5ff21-101">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5ff21-101">New-AzureStorageContext</span></span>

## <span data-ttu-id="5ff21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ff21-102">SYNOPSIS</span></span>
<span data-ttu-id="5ff21-103">Erstellt einen Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="5ff21-103">Creates an Azure Storage context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ff21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ff21-104">SYNTAX</span></span>

### <span data-ttu-id="5ff21-105">AccountNameAndKey (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ff21-105">AccountNameAndKey (Default)</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="5ff21-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="5ff21-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="5ff21-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="5ff21-107">AnonymousAccount</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ff21-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="5ff21-108">AnonymousAccountEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="5ff21-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="5ff21-109">SasToken</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="5ff21-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="5ff21-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzureStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="5ff21-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5ff21-111">ConnectionString</span></span>
```
New-AzureStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="5ff21-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="5ff21-112">LocalDevelopment</span></span>
```
New-AzureStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="5ff21-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ff21-113">DESCRIPTION</span></span>
<span data-ttu-id="5ff21-114">Das Cmdlet **New-AzureStorageContext** erstellt einen Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="5ff21-114">The **New-AzureStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="5ff21-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ff21-115">EXAMPLES</span></span>

### <span data-ttu-id="5ff21-116">Beispiel 1: Erstellen eines Kontexts durch Angeben eines Speicherkonto namens und-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="5ff21-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="5ff21-117">Dieser Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ff21-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="5ff21-118">Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="5ff21-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzureStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="5ff21-119">Dieser Befehl erstellt einen Kontext basierend auf der angegebenen Verbindungszeichenfolge für das Konto ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="5ff21-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="5ff21-120">Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="5ff21-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="5ff21-121">Dieser Befehl erstellt einen Kontext für die anonyme Verwendung für das Konto mit dem Namen ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="5ff21-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="5ff21-122">Der Befehl gibt HTTP als Verbindungsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="5ff21-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="5ff21-123">Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen entwicklungsspeicher Kontos</span><span class="sxs-lookup"><span data-stu-id="5ff21-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local
```

<span data-ttu-id="5ff21-124">Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos.</span><span class="sxs-lookup"><span data-stu-id="5ff21-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="5ff21-125">Der Befehl gibt den *lokalen* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="5ff21-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="5ff21-126">Beispiel 5: Abrufen des Containers für das lokale Entwickler Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="5ff21-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzureStorageContext -Local | Get-AzureStorageContainer
```

<span data-ttu-id="5ff21-127">Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und übergibt dann den neuen Kontext mithilfe des Pipelineoperators an das Cmdlet " **Get-AzureStorageContainer** ".</span><span class="sxs-lookup"><span data-stu-id="5ff21-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzureStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5ff21-128">Der Befehl ruft den Azure-Speichercontainer für das lokale Entwickler Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="5ff21-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="5ff21-129">Beispiel 6: Abrufen mehrerer Container</span><span class="sxs-lookup"><span data-stu-id="5ff21-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzureStorageContext -Local 
PS C:\> $Context02 = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzureStorageContainer
```

<span data-ttu-id="5ff21-130">Der erste Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und speichert diesen Kontext dann in der $Context 01-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ff21-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="5ff21-131">Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird, und speichert diesen Kontext dann in der Variablen $Context 02.</span><span class="sxs-lookup"><span data-stu-id="5ff21-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="5ff21-132">Der endgültige Befehl ruft die Container für die in $context 01 und $Context 02 gespeicherten Kontexte ab, indem **Sie Get-AzureStorageContainer** verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ff21-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="5ff21-133">Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="5ff21-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="5ff21-134">Dieser Befehl erstellt einen Azure-Speicherkontext mit dem angegebenen Speicher Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="5ff21-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="5ff21-135">Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ff21-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="5ff21-136">Beispiel 8: Erstellen eines Kontexts mit einer angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="5ff21-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="5ff21-137">Mit diesem Befehl wird ein Azure-Speicherkontext mit der angegebenen Azure-Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ff21-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="5ff21-138">Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5ff21-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="5ff21-139">Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="5ff21-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzureStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzureStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="5ff21-140">Der erste Befehl generiert ein SAS-Token mithilfe des Cmdlets **New-AzureStorageContainerSASToken** für den Container mit dem Namen ContosoMain und speichert dieses Token dann in der $SasToken-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ff21-140">The first command generates an SAS token by using the **New-AzureStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="5ff21-141">Dieses Token dient zum Lesen, hinzufügen, aktualisieren und Löschen von Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="5ff21-141">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="5ff21-142">Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, das das in $SasToken gespeicherte SAS-Token verwendet, und speichert diesen Kontext dann in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="5ff21-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="5ff21-143">Der endgültige Befehl listet alle BLOBs auf, die dem Container mit dem Namen ContosoMain zugeordnet sind, indem Sie den in $context gespeicherten Kontext verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ff21-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="5ff21-144">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ff21-144">PARAMETERS</span></span>

### <span data-ttu-id="5ff21-145">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="5ff21-145">-Anonymous</span></span>
<span data-ttu-id="5ff21-146">Gibt an, dass mit diesem Cmdlet ein Azure-Speicherkontext für die anonyme Anmeldung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="5ff21-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff21-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="5ff21-147">-ConnectionString</span></span>
<span data-ttu-id="5ff21-148">Gibt eine Verbindungszeichenfolge für den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5ff21-148">Specifies a connection string for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff21-149">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="5ff21-149">-Endpoint</span></span>
<span data-ttu-id="5ff21-150">Gibt den Endpunkt für den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="5ff21-150">Specifies the endpoint for the Azure Storage context.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff21-151">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="5ff21-151">-Environment</span></span>
<span data-ttu-id="5ff21-152">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="5ff21-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="5ff21-153">Die zulässigen Werte für diesen Parameter sind: AzureCloud und AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="5ff21-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="5ff21-154">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="5ff21-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ff21-155">-Lokal</span><span class="sxs-lookup"><span data-stu-id="5ff21-155">-Local</span></span>
<span data-ttu-id="5ff21-156">Gibt an, dass dieses Cmdlet einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ff21-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff21-157">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="5ff21-157">-Protocol</span></span>
<span data-ttu-id="5ff21-158">Übertragungsprotokoll (HTTPS/HTTP).</span><span class="sxs-lookup"><span data-stu-id="5ff21-158">Transfer Protocol (https/http).</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff21-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="5ff21-159">-SasToken</span></span>
<span data-ttu-id="5ff21-160">Gibt ein SAS-Token (Shared Access Signature) für den Kontext an.</span><span class="sxs-lookup"><span data-stu-id="5ff21-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff21-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="5ff21-161">-StorageAccountKey</span></span>
<span data-ttu-id="5ff21-162">Gibt einen Azure-speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="5ff21-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="5ff21-163">Dieses Cmdlet erstellt einen Kontext für den Schlüssel, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5ff21-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff21-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5ff21-164">-StorageAccountName</span></span>
<span data-ttu-id="5ff21-165">Gibt den Namen eines Azure-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="5ff21-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="5ff21-166">Dieses Cmdlet erstellt einen Kontext für das Konto, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5ff21-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ff21-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ff21-167">CommonParameters</span></span>
<span data-ttu-id="5ff21-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ff21-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ff21-169">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ff21-169">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ff21-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ff21-170">INPUTS</span></span>

### <span data-ttu-id="5ff21-171">System. String</span><span class="sxs-lookup"><span data-stu-id="5ff21-171">System.String</span></span>

## <span data-ttu-id="5ff21-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ff21-172">OUTPUTS</span></span>

### <span data-ttu-id="5ff21-173">Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5ff21-173">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="5ff21-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ff21-174">NOTES</span></span>

## <span data-ttu-id="5ff21-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ff21-175">RELATED LINKS</span></span>

[<span data-ttu-id="5ff21-176">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="5ff21-176">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="5ff21-177">Neu – AzureStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="5ff21-177">New-AzureStorageContainerSASToken</span></span>](./New-AzureStorageContainerSASToken.md)


