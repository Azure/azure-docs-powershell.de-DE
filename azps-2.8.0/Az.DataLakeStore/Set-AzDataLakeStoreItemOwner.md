---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 415C5854-FE03-4D4E-BE84-408EA5F95E34
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemOwner.md
ms.openlocfilehash: 446bd86eb37e45d3b4b302fdedf46e1cbe05e51c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651504"
---
# <span data-ttu-id="86716-101">Set-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="86716-101">Set-AzDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="86716-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86716-102">SYNOPSIS</span></span>
<span data-ttu-id="86716-103">Ändert den Besitzer einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="86716-103">Modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="86716-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86716-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-Id] <Guid> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86716-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86716-105">DESCRIPTION</span></span>
<span data-ttu-id="86716-106">Das Cmdlet " **Satz-AzDataLakeStoreItemOwner** " ändert den Besitzer einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="86716-106">The **Set-AzDataLakeStoreItemOwner** cmdlet modifies the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="86716-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86716-107">EXAMPLES</span></span>

### <span data-ttu-id="86716-108">Beispiel 1: Einrichten des Besitzers für ein Element</span><span class="sxs-lookup"><span data-stu-id="86716-108">Example 1: Set the owner for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="86716-109">Dieser Befehl legt den Besitzer für das Stammverzeichnis auf Patti Fuller fest.</span><span class="sxs-lookup"><span data-stu-id="86716-109">This command sets the owner for the root directory to Patti Fuller.</span></span>

## <span data-ttu-id="86716-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="86716-110">PARAMETERS</span></span>

### <span data-ttu-id="86716-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="86716-111">-Account</span></span>
<span data-ttu-id="86716-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="86716-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86716-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86716-113">-DefaultProfile</span></span>
<span data-ttu-id="86716-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="86716-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86716-115">-ID</span><span class="sxs-lookup"><span data-stu-id="86716-115">-Id</span></span>
<span data-ttu-id="86716-116">Gibt die Objekt-ID des AzureActive-Verzeichnis Benutzers, der Gruppe oder des Dienst Prinzipals an, der als Besitzer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="86716-116">Specifies the object ID of the AzureActive Directory user, group, or service principal to use as the owner.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86716-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86716-117">-PassThru</span></span>
<span data-ttu-id="86716-118">Gibt an, dass der resultierende aktualisierte Besitzer zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="86716-118">Indicates the resulting updated owner should be returned.</span></span>

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

### <span data-ttu-id="86716-119">-Path</span><span class="sxs-lookup"><span data-stu-id="86716-119">-Path</span></span>
<span data-ttu-id="86716-120">Gibt den Daten See-Speicherpfad des zu ändernden Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="86716-120">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86716-121">-Typ</span><span class="sxs-lookup"><span data-stu-id="86716-121">-Type</span></span>
<span data-ttu-id="86716-122">Gibt den Typ des festzulegenden Besitzers an.</span><span class="sxs-lookup"><span data-stu-id="86716-122">Specifies the type of owner to set.</span></span>
<span data-ttu-id="86716-123">Die zulässigen Werte für diesen Parameter sind: Benutzer und Gruppe.</span><span class="sxs-lookup"><span data-stu-id="86716-123">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86716-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86716-124">-Confirm</span></span>
<span data-ttu-id="86716-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86716-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86716-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86716-126">-WhatIf</span></span>
<span data-ttu-id="86716-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86716-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86716-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86716-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86716-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86716-129">CommonParameters</span></span>
<span data-ttu-id="86716-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86716-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86716-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86716-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86716-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86716-132">INPUTS</span></span>

### <span data-ttu-id="86716-133">System. String</span><span class="sxs-lookup"><span data-stu-id="86716-133">System.String</span></span>

### <span data-ttu-id="86716-134">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="86716-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="86716-135">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Besitzer</span><span class="sxs-lookup"><span data-stu-id="86716-135">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

### <span data-ttu-id="86716-136">System. GUID</span><span class="sxs-lookup"><span data-stu-id="86716-136">System.Guid</span></span>

### <span data-ttu-id="86716-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="86716-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86716-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86716-138">OUTPUTS</span></span>

### <span data-ttu-id="86716-139">System. String</span><span class="sxs-lookup"><span data-stu-id="86716-139">System.String</span></span>

## <span data-ttu-id="86716-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="86716-140">NOTES</span></span>

## <span data-ttu-id="86716-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86716-141">RELATED LINKS</span></span>

[<span data-ttu-id="86716-142">Get-AzDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="86716-142">Get-AzDataLakeStoreItemOwner</span></span>](./Get-AzDataLakeStoreItemOwner.md)


