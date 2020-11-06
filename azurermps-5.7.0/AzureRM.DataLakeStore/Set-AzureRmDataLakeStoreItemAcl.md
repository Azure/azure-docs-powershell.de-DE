---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 313813bec61dac2f5b41f7ad2d36e5ee5ba1b44f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479809"
---
# <span data-ttu-id="a579e-101">Set-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="a579e-101">Set-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="a579e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a579e-102">SYNOPSIS</span></span>
<span data-ttu-id="a579e-103">Ändert die ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a579e-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a579e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a579e-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a579e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a579e-105">DESCRIPTION</span></span>
<span data-ttu-id="a579e-106">Das Cmdlet " **festlegen-AzureRmDataLakeStoreItemAcl** " ändert die Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a579e-106">The **Set-AzureRmDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a579e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a579e-107">EXAMPLES</span></span>

### <span data-ttu-id="a579e-108">Beispiel 1: Einrichten der ACL für eine Datei und einen Ordner</span><span class="sxs-lookup"><span data-stu-id="a579e-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path /
PS C:\> Set-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="a579e-109">Der erste Befehl ruft die ACL für das Stammverzeichnis des ContosoADL-Kontos ab und speichert es dann in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a579e-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>

<span data-ttu-id="a579e-110">Der zweite Befehl legt die ACL für die Datei Test.txt auf diejenige in $ACL fest.</span><span class="sxs-lookup"><span data-stu-id="a579e-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

## <span data-ttu-id="a579e-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a579e-111">PARAMETERS</span></span>

### <span data-ttu-id="a579e-112">-Konto</span><span class="sxs-lookup"><span data-stu-id="a579e-112">-Account</span></span>
<span data-ttu-id="a579e-113">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="a579e-113">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-114">-ACL</span><span class="sxs-lookup"><span data-stu-id="a579e-114">-Acl</span></span>
<span data-ttu-id="a579e-115">Gibt eine Zugriffssteuerungsliste für eine Datei oder einen Ordner an.</span><span class="sxs-lookup"><span data-stu-id="a579e-115">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a579e-116">-DefaultProfile</span></span>
<span data-ttu-id="a579e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a579e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a579e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a579e-118">-PassThru</span></span>
<span data-ttu-id="a579e-119">Gibt an, dass die resultierende ACL zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a579e-119">Indicates the resulting ACL should be returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-120">-Path</span><span class="sxs-lookup"><span data-stu-id="a579e-120">-Path</span></span>
<span data-ttu-id="a579e-121">Gibt den Daten See-Speicherpfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="a579e-121">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a579e-122">-Confirm</span></span>
<span data-ttu-id="a579e-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a579e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a579e-124">-WhatIf</span></span>
<span data-ttu-id="a579e-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a579e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a579e-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a579e-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a579e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a579e-127">CommonParameters</span></span>
<span data-ttu-id="a579e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a579e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a579e-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a579e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a579e-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a579e-130">INPUTS</span></span>

### <span data-ttu-id="a579e-131">DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="a579e-131">DataLakeStoreItemAce[]</span></span>
<span data-ttu-id="a579e-132">Der Parameter "ACL" akzeptiert den Wert vom Typ "DataLakeStoreItemAce []" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a579e-132">Parameter 'Acl' accepts value of type 'DataLakeStoreItemAce[]' from the pipeline</span></span>

## <span data-ttu-id="a579e-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a579e-133">OUTPUTS</span></span>

### <span data-ttu-id="a579e-134">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="a579e-134">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="a579e-135">Wenn passthru angegeben wird, gibt die resultierende Liste der ACL-Einträge zurück.</span><span class="sxs-lookup"><span data-stu-id="a579e-135">If PassThru is specified, will return the resulting list of ACL entries.</span></span>

## <span data-ttu-id="a579e-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="a579e-136">NOTES</span></span>

## <span data-ttu-id="a579e-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a579e-137">RELATED LINKS</span></span>

