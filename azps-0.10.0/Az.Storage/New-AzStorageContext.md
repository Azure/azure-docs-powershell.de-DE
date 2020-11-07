---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae22e6923a03864b9371ccdf5379ef9b6bf5189d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843008"
---
# <span data-ttu-id="04b90-101">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="04b90-101">New-AzStorageContext</span></span>

## <span data-ttu-id="04b90-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04b90-102">SYNOPSIS</span></span>
<span data-ttu-id="04b90-103">Erstellt einen Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="04b90-103">Creates an Azure Storage context.</span></span>

## <span data-ttu-id="04b90-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04b90-104">SYNTAX</span></span>

### <span data-ttu-id="04b90-105">AccountNameAndKey (Standard)</span><span class="sxs-lookup"><span data-stu-id="04b90-105">AccountNameAndKey (Default)</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="04b90-106">AccountNameAndKeyEnvironment</span><span class="sxs-lookup"><span data-stu-id="04b90-106">AccountNameAndKeyEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### <span data-ttu-id="04b90-107">AnonymousAccount</span><span class="sxs-lookup"><span data-stu-id="04b90-107">AnonymousAccount</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="04b90-108">AnonymousAccountEnvironment</span><span class="sxs-lookup"><span data-stu-id="04b90-108">AnonymousAccountEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="04b90-109">SasToken</span><span class="sxs-lookup"><span data-stu-id="04b90-109">SasToken</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### <span data-ttu-id="04b90-110">SasTokenWithAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="04b90-110">SasTokenWithAzureEnvironment</span></span>
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### <span data-ttu-id="04b90-111">ConnectionString</span><span class="sxs-lookup"><span data-stu-id="04b90-111">ConnectionString</span></span>
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### <span data-ttu-id="04b90-112">LocalDevelopment</span><span class="sxs-lookup"><span data-stu-id="04b90-112">LocalDevelopment</span></span>
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## <span data-ttu-id="04b90-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04b90-113">DESCRIPTION</span></span>
<span data-ttu-id="04b90-114">Das Cmdlet **New-AzStorageContext** erstellt einen Azure-Speicherkontext.</span><span class="sxs-lookup"><span data-stu-id="04b90-114">The **New-AzStorageContext** cmdlet creates an Azure Storage context.</span></span>

## <span data-ttu-id="04b90-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04b90-115">EXAMPLES</span></span>

### <span data-ttu-id="04b90-116">Beispiel 1: Erstellen eines Kontexts durch Angeben eines Speicherkonto namens und-Schlüssels</span><span class="sxs-lookup"><span data-stu-id="04b90-116">Example 1: Create a context by specifying a storage account name and key</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

<span data-ttu-id="04b90-117">Dieser Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04b90-117">This command creates a context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="04b90-118">Beispiel 2: Erstellen eines Kontexts durch Angeben einer Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="04b90-118">Example 2: Create a context by specifying a connection string</span></span>
```
C:\PS>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

<span data-ttu-id="04b90-119">Dieser Befehl erstellt einen Kontext basierend auf der angegebenen Verbindungszeichenfolge für das Konto ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="04b90-119">This command creates a context based on the specified connection string for the account ContosoGeneral.</span></span>

### <span data-ttu-id="04b90-120">Beispiel 3: Erstellen eines Kontexts für ein anonymes Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="04b90-120">Example 3: Create a context for an anonymous storage account</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

<span data-ttu-id="04b90-121">Dieser Befehl erstellt einen Kontext für die anonyme Verwendung für das Konto mit dem Namen ContosoGeneral.</span><span class="sxs-lookup"><span data-stu-id="04b90-121">This command creates a context for anonymous use for the account named ContosoGeneral.</span></span>
<span data-ttu-id="04b90-122">Der Befehl gibt HTTP als Verbindungsprotokoll an.</span><span class="sxs-lookup"><span data-stu-id="04b90-122">The command specifies HTTP as a connection protocol.</span></span>

### <span data-ttu-id="04b90-123">Beispiel 4: Erstellen eines Kontexts mithilfe des lokalen entwicklungsspeicher Kontos</span><span class="sxs-lookup"><span data-stu-id="04b90-123">Example 4: Create a context by using the local development storage account</span></span>
```
C:\PS>New-AzStorageContext -Local
```

<span data-ttu-id="04b90-124">Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos.</span><span class="sxs-lookup"><span data-stu-id="04b90-124">This command creates a context by using the local development storage account.</span></span>
<span data-ttu-id="04b90-125">Der Befehl gibt den *lokalen* Parameter an.</span><span class="sxs-lookup"><span data-stu-id="04b90-125">The command specifies the *Local* parameter.</span></span>

### <span data-ttu-id="04b90-126">Beispiel 5: Abrufen des Containers für das lokale Entwickler Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="04b90-126">Example 5: Get the container for the local developer storage account</span></span>
```
C:\PS>New-AzStorageContext -Local | Get-AzStorageContainer
```

<span data-ttu-id="04b90-127">Dieser Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und übergibt dann den neuen Kontext mithilfe des Pipelineoperators an das Cmdlet " **Get-AzStorageContainer** ".</span><span class="sxs-lookup"><span data-stu-id="04b90-127">This command creates a context by using the local development storage account, and then passes the new context to the **Get-AzStorageContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="04b90-128">Der Befehl ruft den Azure-Speichercontainer für das lokale Entwickler Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="04b90-128">The command gets the Azure Storage container for the local developer storage account.</span></span>

### <span data-ttu-id="04b90-129">Beispiel 6: Abrufen mehrerer Container</span><span class="sxs-lookup"><span data-stu-id="04b90-129">Example 6: Get multiple containers</span></span>
```
C:\PS>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

<span data-ttu-id="04b90-130">Der erste Befehl erstellt einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos und speichert diesen Kontext dann in der $Context 01-Variablen.</span><span class="sxs-lookup"><span data-stu-id="04b90-130">The first command creates a context by using the local development storage account, and then stores that context in the $Context01 variable.</span></span>
<span data-ttu-id="04b90-131">Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird, und speichert diesen Kontext dann in der Variablen $Context 02.</span><span class="sxs-lookup"><span data-stu-id="04b90-131">The second command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that context in the $Context02 variable.</span></span>
<span data-ttu-id="04b90-132">Der endgültige Befehl ruft die Container für die in $context 01 und $Context 02 gespeicherten Kontexte ab, indem **Sie Get-AzStorageContainer** verwenden.</span><span class="sxs-lookup"><span data-stu-id="04b90-132">The final command gets the containers for the contexts stored in $Context01 and $Context02 by using **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="04b90-133">Beispiel 7: Erstellen eines Kontexts mit einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="04b90-133">Example 7: Create a context with an endpoint</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

<span data-ttu-id="04b90-134">Dieser Befehl erstellt einen Azure-Speicherkontext mit dem angegebenen Speicher Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="04b90-134">This command creates an Azure Storage context that has the specified storage endpoint.</span></span>
<span data-ttu-id="04b90-135">Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04b90-135">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="04b90-136">Beispiel 8: Erstellen eines Kontexts mit einer angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="04b90-136">Example 8: Create a context with a specified environment</span></span>
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

<span data-ttu-id="04b90-137">Mit diesem Befehl wird ein Azure-Speicherkontext mit der angegebenen Azure-Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="04b90-137">This command creates an Azure storage context that has the specified Azure environment.</span></span>
<span data-ttu-id="04b90-138">Der Befehl erstellt den Kontext für das Konto mit dem Namen ContosoGeneral, in dem der angegebene Schlüssel verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="04b90-138">The command creates the context for the account named ContosoGeneral that uses the specified key.</span></span>

### <span data-ttu-id="04b90-139">Beispiel 9: Erstellen eines Kontexts mithilfe eines SAS-Tokens</span><span class="sxs-lookup"><span data-stu-id="04b90-139">Example 9: Create a context by using an SAS token</span></span>
```
C:\PS>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

<span data-ttu-id="04b90-140">Der erste Befehl generiert ein SAS-Token mithilfe des Cmdlets **New-AzStorageContainerSASToken** für den Container mit dem Namen ContosoMain und speichert dieses Token dann in der $SasToken-Variablen.</span><span class="sxs-lookup"><span data-stu-id="04b90-140">The first command generates an SAS token by using the **New-AzStorageContainerSASToken** cmdlet for the container named ContosoMain, and then stores that token in the $SasToken variable.</span></span>
<span data-ttu-id="04b90-141">Dieses Token dient zum Lesen, hinzufügen, aktualisieren und Löschen von Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="04b90-141">That token is for read, add, update, and delete permissions.</span></span>
<span data-ttu-id="04b90-142">Der zweite Befehl erstellt einen Kontext für das Konto mit dem Namen ContosoGeneral, das das in $SasToken gespeicherte SAS-Token verwendet, und speichert diesen Kontext dann in der $Context Variablen.</span><span class="sxs-lookup"><span data-stu-id="04b90-142">The second command creates a context for the account named ContosoGeneral that uses the SAS token stored in $SasToken, and then stores that context in the $Context variable.</span></span>
<span data-ttu-id="04b90-143">Der endgültige Befehl listet alle BLOBs auf, die dem Container mit dem Namen ContosoMain zugeordnet sind, indem Sie den in $context gespeicherten Kontext verwenden.</span><span class="sxs-lookup"><span data-stu-id="04b90-143">The final command lists all the blobs associated with the container named ContosoMain by using the context stored in $Context.</span></span>

## <span data-ttu-id="04b90-144">Parameter</span><span class="sxs-lookup"><span data-stu-id="04b90-144">PARAMETERS</span></span>

### <span data-ttu-id="04b90-145">-Anonymous</span><span class="sxs-lookup"><span data-stu-id="04b90-145">-Anonymous</span></span>
<span data-ttu-id="04b90-146">Gibt an, dass mit diesem Cmdlet ein Azure-Speicherkontext für die anonyme Anmeldung erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="04b90-146">Indicates that this cmdlet creates an Azure Storage context for anonymous logon.</span></span>

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

### <span data-ttu-id="04b90-147">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="04b90-147">-ConnectionString</span></span>
<span data-ttu-id="04b90-148">Gibt eine Verbindungszeichenfolge für den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="04b90-148">Specifies a connection string for the Azure Storage context.</span></span>

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

### <span data-ttu-id="04b90-149">-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="04b90-149">-Endpoint</span></span>
<span data-ttu-id="04b90-150">Gibt den Endpunkt für den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="04b90-150">Specifies the endpoint for the Azure Storage context.</span></span>

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

### <span data-ttu-id="04b90-151">-Umgebung</span><span class="sxs-lookup"><span data-stu-id="04b90-151">-Environment</span></span>
<span data-ttu-id="04b90-152">Gibt die Azure-Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="04b90-152">Specifies the Azure environment.</span></span>
<span data-ttu-id="04b90-153">Die zulässigen Werte für diesen Parameter sind: AzureCloud und AzureChinaCloud.</span><span class="sxs-lookup"><span data-stu-id="04b90-153">The acceptable values for this parameter are: AzureCloud and AzureChinaCloud.</span></span>
<span data-ttu-id="04b90-154">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-AzureEnvironment` .</span><span class="sxs-lookup"><span data-stu-id="04b90-154">For more information, type `Get-Help Get-AzureEnvironment`.</span></span>

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

### <span data-ttu-id="04b90-155">-Lokal</span><span class="sxs-lookup"><span data-stu-id="04b90-155">-Local</span></span>
<span data-ttu-id="04b90-156">Gibt an, dass dieses Cmdlet einen Kontext mithilfe des lokalen entwicklungsspeicher Kontos erstellt.</span><span class="sxs-lookup"><span data-stu-id="04b90-156">Indicates that this cmdlet creates a context by using the local development storage account.</span></span>

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

### <span data-ttu-id="04b90-157">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="04b90-157">-Protocol</span></span>
<span data-ttu-id="04b90-158">Übertragungsprotokoll (HTTPS/HTTP).</span><span class="sxs-lookup"><span data-stu-id="04b90-158">Transfer Protocol (https/http).</span></span>

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

### <span data-ttu-id="04b90-159">-SasToken</span><span class="sxs-lookup"><span data-stu-id="04b90-159">-SasToken</span></span>
<span data-ttu-id="04b90-160">Gibt ein SAS-Token (Shared Access Signature) für den Kontext an.</span><span class="sxs-lookup"><span data-stu-id="04b90-160">Specifies a Shared Access Signature (SAS) token for the context.</span></span>

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

### <span data-ttu-id="04b90-161">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="04b90-161">-StorageAccountKey</span></span>
<span data-ttu-id="04b90-162">Gibt einen Azure-speicherkontoschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="04b90-162">Specifies an Azure Storage account key.</span></span>
<span data-ttu-id="04b90-163">Dieses Cmdlet erstellt einen Kontext für den Schlüssel, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="04b90-163">This cmdlet creates a context for the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="04b90-164">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04b90-164">-StorageAccountName</span></span>
<span data-ttu-id="04b90-165">Gibt den Namen eines Azure-speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="04b90-165">Specifies an Azure Storage account name.</span></span>
<span data-ttu-id="04b90-166">Dieses Cmdlet erstellt einen Kontext für das Konto, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="04b90-166">This cmdlet creates a context for the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="04b90-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b90-167">CommonParameters</span></span>
<span data-ttu-id="04b90-168">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04b90-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b90-169">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04b90-169">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b90-170">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04b90-170">INPUTS</span></span>

### <span data-ttu-id="04b90-171">System. String</span><span class="sxs-lookup"><span data-stu-id="04b90-171">System.String</span></span>

## <span data-ttu-id="04b90-172">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04b90-172">OUTPUTS</span></span>

### <span data-ttu-id="04b90-173">Microsoft. WindowsAzure. Commands. Storage. AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="04b90-173">Microsoft.WindowsAzure.Commands.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="04b90-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="04b90-174">NOTES</span></span>

## <span data-ttu-id="04b90-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04b90-175">RELATED LINKS</span></span>

[<span data-ttu-id="04b90-176">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="04b90-176">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="04b90-177">Neu – AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="04b90-177">New-AzStorageContainerSASToken</span></span>](./New-AzStorageContainerSASToken.md)


